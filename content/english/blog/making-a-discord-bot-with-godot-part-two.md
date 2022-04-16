---
title: "Making a Discord Bot with Godot (Part Two)"
date: 2019-07-03T22:27:32+03:00
author: Emmanouil Papadeas
image: images/blog/making-a-discord-bot-in-godot/godot.webp
---

This is a continuation from Part One, which you can find [here](../making-a-discord-bot-with-godot-part-one).

Back for more I see? In the second part of this blog tutorial series we’re going to handle **resuming** our connection in case of a disconnection, disconnect in purpose if we don’t receive a **Heartbeat ACK**, and handle **Opcode 9 Invalid Session** payloads. So, let’s *resume* the tutorial! (See what I did there? Resume? Anyway, moving on)

Before we even begin, the first thing I’m going to do is rename our Timer node to “HeartbeatTimer”, have the heartbeat_interval variable converted to seconds from the moment we set a value for it (by doing `heartbeat_interval = dict["d"]["heartbeat_interval"] / 1000`), and replace the code inside our Opcode 0 Dispatch with a neat looking `handle_events(dict: Dictionary)` method. All the previous code will be put inside that new method, which will be used to, well, handle our events. The first event we’re going to handle is our Ready event. We’re going to need a new String variable called session_id, which we need in order to resume our connection. So, inside our new method, store the “t” field of our dictionary (this is the name of the event) and check if it is equal to “READY”. If it is, set our session_id variable to `dict["d"]["session_id"]`. Behold, it’s screenshot time!

![](../../images/blog/making-a-discord-bot-in-godot/6.webp)

Ah, much better. Reminder that this is inside our `_data_received()` method.

![](../../images/blog/making-a-discord-bot-in-godot/7.webp)
And our new baby, `handle_events()`. Don’t forget to initialize session_id as a String variable at the top of our script!

All is going well and our bot is work- nope, we disconnected. Oh well, that happens all the time anyway. So, how do we handle it? Well first of all, we need to tell our client to reconnect. So, in our process method, we and an else statement to check if the client is disconnected, and if it is, we tell it to connect to the Gateway’s URL. Oh, and before I forget, we can connect the WebSocketClient’s connection_closed and server_close_request signals to two new methods. Τhe first method will just print to the console that we got disconnected, and the second one will print that the server has requested a clean close, along with the [close event code and reason](https://discordapp.com/developers/docs/topics/opcodes-and-status-codes#gateway-gateway-close-event-codes). If the client manages to connect again, it will receive an Opcode 10 Hello payload. We don’t, however, have to identify ourselves again. We can do a check if we have a session_id, and if we do, we can send an Opcode 6 Resume payload to the Gateway instead. The 3 fields that are required for that payload is the bot’s **token**, the **session_id** and the **last_sequence** number.
![](../../images/blog/making-a-discord-bot-in-godot/8.webp)
Our new else statement inside our process method.

![](../../images/blog/making-a-discord-bot-in-godot/9.webp)
Updated our Opcode 10 Hello logic to handle resuming.

Now that we’re done with resuming, we’ll disconnect on purpose. Wait, what? Why? Because that’s what the [Discord Developer Docs](https://discordapp.com/developers/docs/topics/gateway#heartbeating) say, my dear viewer!
“If a client does not receive a heartbeat ack between its attempts at sending heartbeats, it should immediately terminate the connection with a non-1000 close code, reconnect, and attempt to resume.“
And that’s exactly what we will do. For that, we need a new boolean variable called **heartbeat_ack_received**, set as true at the top of our script. We will set the variable as false every time we send an Opcode 1 Heartbeat payload, and then back to true when we receive an Opcode 11 Heartbeat ACK payload. Now, we have to check if the variable has remained false when we are about to send our next Opcode 1 Heartbeat. If it is false, meaning we haven’t received an Opcode 11 Heartbeat ACK, we terminate the connection with a non-1000 code and return from the method. To be honest, I don’t know if that is the best way of handling the situation, so, if you have any better ideas be sure to comment them down below! Some screenshots for your the pleasure of your eyes.

![](../../images/blog/making-a-discord-bot-in-godot/10.webp)
Remember to initialize your variables at the top of the script, kids.

![](../../images/blog/making-a-discord-bot-in-godot/11.webp)
Set heartbeat_ack_received to true when we RECEIVE a Heartbeat ACK

![](../../images/blog/making-a-discord-bot-in-godot/12.webp)
We check if heartbeat_ack_received is false when we are about to send a Heartbeat, and if it is, we terminate our connection with code 1002 (any non-1000 code should work fine? I guess?) and return from the method. If it is true, we send our Heartbeat as we usually would and we set heartbeat_ack_received to false.

And I think that’s it for handling disconnections, when we don’t receive Heartbeat ACK payloads. Last up for this part is handling Opcode 9 Invalid Session payloads. You can find more info on them on [Discord’s docs](https://discordapp.com/developers/docs/topics/gateway#invalid-session). This is again something that I’m not sure if my method is the best way of doing it, so if you have any objections, make sure to comment! Following instructions from the docs, when we  receive an **Opcode 9 Invalid Session** payload, we have to wait a random time between 1 and 5 seconds, and then re-identify ourselves. Well, if the “d” field is false, that is. “d” is a boolean that indicates whether the session may be resumable.  So if “d” is true, we’ll resume instead of re-identifying. So, we’ll create a new boolean variable at the top of our script called **invalid_session_is_resumable**, and at our ready method we’ll call `randomize()`, so the time the client has to wait after receiving the Opcode 9 payload will always be random. Then, we’ll create a new Timer Node as a child, which we will call “InvalidSessionTimer”, and we’ll do a new check to see if our op code is equal to “9”. If it is, we’ll set invalid_session_is_resumable to be equal to the “d” field of the payload, and we’ll set the InvalidSessionTimer’s wait time to `rand_range(1,5)`. We also need to make the timer’s `one_shot = true`, because we only want it to run only once every time we get an Opcode 9 Invalid Session payload, and then finally start it. We’ll connect InvalidSessionTimer’s timeout signal to a new method inside our script, where we’ll do pretty much the same we do with handling Opcode 10 Hello payloads, except the “setting up to send heartbeats” part. We’ll check if the invalid session is resumable AND if we have a session_id. If both are true, we’ll send a Resume payload. If at least one of them is false, we’ll send an Identify payload. Finally, it’s screenshot time.

![](../../images/blog/making-a-discord-bot-in-godot/13.webp)

Don’t forget to declare the boolean variable at the top of the script and to call `randomize()`!

![](../../images/blog/making-a-discord-bot-in-godot/14.webp)
 And I op- New code for handling Invalid Sessions

![](../../images/blog/making-a-discord-bot-in-godot/15.webp)
Timeout method for InvalidSessionTimer

That’s all folks! For this part at least. You can find the [code in pastebin](https://pastebin.com/4yvDu4nU)! Next up we have receiving messages and having the bot responding. Yes, time for some socialization! Make sure to follow this blog so you don’t miss the next part! See you then!
