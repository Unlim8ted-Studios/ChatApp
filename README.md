# ChatApp

A small Python chat app for talking with people on the same network.

It uses a simple client/server setup with a Pygame interface and includes an animated weather-style background while you chat.

## Features

- Real-time messaging between multiple users
- Local network server discovery
- Custom usernames
- Basic message history for newly connected users
- Pygame-based interface
- Animated rain and weather effects
- Separate client and server programs

## How It Works

One computer runs `server.py`.

Other computers on the same network run `client.py` and connect to the server. The client can scan the local network for available servers, or you can enter an IP address manually.

Messages are sent to the server and then forwarded to the other connected clients.

The server currently uses port `9999`.

## Requirements

- Python 3
- Pygame
- pywin32

Install the dependencies with:

```bash
pip install pygame pywin32
```

The current version is primarily built for Windows.

## Running the App

### 1. Start the server

On the computer that will host the chat:

```bash
python server.py
```

The server will begin listening for connections.

### 2. Start a client

On another computer:

```bash
python client.py
```

The client will look for servers on the local network.

Select the server, enter a username, and start chatting.

You can also enter a server IP manually from the terminal.

## Weather Effects

The client includes a small animated background system originally made to give the chat window a little more personality.

The current version includes code for:

- Rain
- Wind
- Thunderstorms
- Lightning
- Clouds
- Leaves

Some of these effects are experimental or currently disabled in the main interface.

## Project Structure

```text
ChatApp/
├── client.py
├── server.py
├── README.md
├── LICENSE
└── LICENCE.md
```

`client.py` contains the chat interface, network discovery, client networking, and visual effects.

`server.py` handles incoming connections, stores the current chat history, and sends messages between clients.

## Notes

This was made as a small experimental project rather than a production messaging app.

Messages are sent directly over the network and the app does not currently include encryption, authentication, accounts, or persistent message storage.

Because of that, it is best used on networks you trust.

## Contributing

If you find a bug or want to improve something, feel free to open an issue or submit a pull request.
