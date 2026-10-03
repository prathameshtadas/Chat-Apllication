# Client-Server Chat Application

A Java **client-server chat application** built with socket programming. Multiple clients can connect to a server and exchange private messages in real time over a local network.

## Features

- Client-server architecture
- Java socket communication using `java.net`
- Multiple simultaneous clients
- Private message routing by recipient name
- Console-based interaction
- Maven project structure

## Tech Stack

- **Java**
- **Socket Programming**
- **TCP Networking**
- **Multithreading**
- **Maven**

## Architecture

```text
                ┌──────────────┐
                │    Server    │
                │ Socket / TCP │
                └──────┬───────┘
                       │
          ┌────────────┼────────────┐
          │            │            │
      ┌───▼───┐    ┌───▼───┐    ┌───▼───┐
      │Client │    │Client │    │Client │
      │   A   │    │   B   │    │   C   │
      └───────┘    └───────┘    └───────┘
```

The server accepts client connections and coordinates message delivery between connected clients.

## Project Structure

```text
Client-Server-Chat-Application-Java-master/
├── pom.xml
├── src/
│   ├── main/
│   │   └── java/
│   └── test/
└── README.md
```

## Requirements

- **JDK 19** or a compatible Java version
- **Maven**

## Run the Project

### Using Maven

From the project directory:

```bash
mvn clean package
```

Then run the server and client entry points from your IDE or Java command line.

### Typical workflow

1. Start the server.
2. Enter the server port.
3. Start one or more clients.
4. Connect clients using the same server port.
5. Send messages using the format:

```text
<receiver name>: <message>
```

Example:

```text
Austin: How are you doing today?
```

## Limitations

- Communication is not encrypted.
- There is no authentication or authorization layer.
- The original project is primarily intended for local-network use.
- Production deployment would require stronger connection management and security controls.

## Future Improvements

- TLS/SSL encrypted communication
- User authentication
- Persistent chat history
- GUI client
- Online/offline presence
- Better connection and exception handling
- Containerized deployment

## Author

**Prathamesh Tadas**

GitHub: https://github.com/prathameshtadas
