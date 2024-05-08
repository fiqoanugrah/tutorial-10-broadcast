## **Hi! :wave:, I'm Muhammad Fiqo Anugrah and this is my repo for Tutorial 10 Adpro C**

> REFLECTION
> Experiment 2.1: Original code, and how it run

### Running Instructions:

1. **Server Setup**:
    - Start the server by running the command `cargo run --bin server` from the terminal.

2. **Client Setup**:
    - Open three separate terminals.
    - In each terminal, execute the command `cargo run --bin client` to launch three clients.

<img width="520" alt="Screenshot 2024-05-08 at 18 01 28" src="https://github.com/fiqoanugrah/tutorial-8-publisher/assets/87713462/3eda5320-31f9-4764-a35a-3a9940931843">
<img width="520" alt="Screenshot 2024-05-08 at 18 01 37" src="https://github.com/fiqoanugrah/tutorial-8-publisher/assets/87713462/9d970047-77bf-4f80-8b7a-bf1bcddee410">
<img width="537" alt="Screenshot 2024-05-08 at 18 01 55" src="https://github.com/fiqoanugrah/tutorial-8-publisher/assets/87713462/ac94cd84-a804-4140-907a-c5eb8f36000b">
<img width="596" alt="Screenshot 2024-05-08 at 18 02 04" src="https://github.com/fiqoanugrah/tutorial-8-publisher/assets/87713462/e7b5e419-7b02-4844-bb60-d2a4d8ae447e">

3. **Message Sending Process**:
    - Any client that types and sends a message will transmit it to the server.
    - The server then receives this message and forwards it to all connected clients.
    - As a result, any message sent by a client is received by all other clients connected to the server through a broadcast process.

<img width="531" alt="Screenshot 2024-05-08 at 18 02 53" src="https://github.com/fiqoanugrah/tutorial-8-publisher/assets/87713462/211b8675-6162-443a-ba52-6cd08a4b5ba1">
<img width="567" alt="Screenshot 2024-05-08 at 18 03 01" src="https://github.com/fiqoanugrah/tutorial-8-publisher/assets/87713462/56d7682f-2a45-4809-a8fb-a972d9a6ca18">
<img width="619" alt="Screenshot 2024-05-08 at 18 03 18" src="https://github.com/fiqoanugrah/tutorial-8-publisher/assets/87713462/86725188-8069-4cb3-b936-a64732bce9d7">
<img width="609" alt="Screenshot 2024-05-08 at 18 03 26" src="https://github.com/fiqoanugrah/tutorial-8-publisher/assets/87713462/bf3dcd62-98c3-4810-a711-a8340f5af265">

### 2.2 Modifying the websocket port
**client.rs:**
<img width="570" alt="Screenshot 2024-05-08 at 18 29 13" src="https://github.com/fiqoanugrah/tutorial-8-publisher/assets/87713462/59c70aee-1db2-4c7b-b57e-1ed3fac7b64a">

**server.rs:**
<img width="741" alt="Screenshot 2024-05-08 at 18 35 09" src="https://github.com/fiqoanugrah/tutorial-8-publisher/assets/87713462/6b4babde-3cd0-40fa-8d6b-c318623520a6">



<img width="787" alt="Screenshot 2024-05-08 at 18 32 50" src="https://github.com/fiqoanugrah/tutorial-8-publisher/assets/87713462/245fd73d-98e4-46eb-aa7a-18c2da16fcfb">
both the client and server share the same port, the program will run smoothly as shown in the image above. if the clients use a different port , the following error will appear in the terminal:
if the server and the client port are different :
<img width="719" alt="Screenshot 2024-05-08 at 18 39 20" src="https://github.com/fiqoanugrah/tutorial-8-publisher/assets/87713462/82252385-960c-4904-9bf6-2a23a0b3b282">


>Experiment 2.3: Small changes, add IP and Port

<img width="517" alt="Screenshot 2024-05-08 at 18 48 17" src="https://github.com/fiqoanugrah/tutorial-10-broadcast/assets/87713462/9907f215-93f9-4e71-8d11-7bd9b3ae7d4f">
<img width="519" alt="Screenshot 2024-05-08 at 18 48 34" src="https://github.com/fiqoanugrah/tutorial-10-broadcast/assets/87713462/d1842310-7594-4e32-927e-d19e73c55639">
The addr variable is a SocketAddress that holds the IP address and port number for each active client. This is used to identify and manage connections uniquely in a networked application. In the client.rs file, modifications have been made to the output formatting
This line of code will now display a message on the console whenever a client connects, showing the client's IP address and port, thus providing clear visibility of each active client's network address. This modification helps in debugging by making it clear which clients are currently connected to the server and from what addresses.


<img width="695" alt="Screenshot 2024-05-08 at 18 51 33" src="https://github.com/fiqoanugrah/tutorial-10-broadcast/assets/87713462/f61c9918-3ace-4d6d-be10-dea5942797a9">