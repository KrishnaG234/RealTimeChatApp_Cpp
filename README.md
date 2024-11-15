# Real-Time Chat Application

This is a simple real-time chat application implemented in C++ using WinSock for network communication. It includes both server and client components, enabling multiple clients to connect to the server and communicate with each other.

## Features

- Real-time message broadcasting to all connected clients.
- Multithreading to handle multiple clients simultaneously.
- Simple and easy-to-understand code structure.

## Requirements

- Windows operating system.
- Visual Studio or any other C++ compiler that supports WinSock.
- WinSock2 library.

## Code Overview

### Server Code

The server code initializes WinSock, creates a listening socket, and waits for client connections. For each client connection, it spawns a new thread to handle communication with that client.

- **Initialization**: The `Initialize()` function initializes WinSock.
- **InteractWithClient()**: Handles communication with a connected client. It receives messages from the client and broadcasts them to all other connected clients.
- **Main Function**: Sets up the server socket, binds it to an address and port, and starts listening for connections. It accepts new clients and creates a new thread for each one.

### Client Code

The client code initializes WinSock, creates a socket, and connects to the server. It uses two threads: one for sending messages and one for receiving messages.

- **Initialization**: The `Initialize()` function initializes WinSock.
- **SendMsg()**: Handles user input and sends messages to the server.
- **ReceiveMsg()**: Receives messages from the server and displays them.
- **Main Function**: Sets up the client socket, connects to the server, and starts the send and receive threads.

## Example Usage

1. Start the server:
    ```sh
    ./server.exe
    ```

2. Start multiple clients in separate terminal windows:
    ```sh
    ./client.exe
    ```

3. Enter your chat name and start chatting!

