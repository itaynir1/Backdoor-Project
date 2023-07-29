
# Backdoor Project

## Description
This project is a simple Python-based tool for remote communication between a client and a server using sockets. The server waits for incoming connections from clients, and once a connection is established, it allows the client to execute shell commands on the server, upload files to the server, and download files from the server.

## Features
- Remote shell access: The client can remotely execute shell commands on the server.
- File upload: The client can upload files to the server.
- File download: The client can download files from the server.
- Basic error handling: The client and server handle errors gracefully.

## Prerequisites
`Python 3.x`

## How to Use
1. First, make sure you have `Python 3.x` installed on both the client and the server machines.

2. Copy the provided client and server code into two separate Python files on their respective machines.

3. Modify the server code to specify the server's IP address and port to bind to (currently set to 192.168.1.63 and 5555, respectively).

4. Run the server script on the server machine. It will wait for incoming connections.

5. Run the client script on the client machine. It will attempt to connect to the server.

6. Once the connection is established, the client will present
a command prompt `(* Shell~%s:)` where %s will show the server's IP address.

7. **Use the following commands to interact with the server:**

`quit` : Disconnect from the server and exit the client.

`clear` : Clear the screen.

`cd <directory>` : Change the current working directory on the server.

`download <file>` : Download a file from the server to the client.

`upload <file>` : Upload a file from the client to the server.

## Example Usage
Assuming the server script is running on `192.168.1.63` , the client script is running on another machine, and they are both in the same local network:

1. Start the server script on the server machine.

2. Start the client script on the client machine.

3. The client will connect to the server, and the server will display `[+] Target Connected From: <client-IP>` .

4. At the client prompt `(* Shell~<server-IP>:)` , you can now enter commands to be executed on the server.

**Example commands** :

- `ls` : List files in the current directory of the server.
- `cd /path/to/directory` : Change the current directory on the server.
- `download file.txt` : Download a file named file.txt from the server to the client.
- `upload local_file.txt` : Upload a file named local_file.txt from the client to the server.

### Note:
This project is intended for educational and learning purposes only. Please use it responsibly and with the consent of the parties involved in the communication. Unauthorized use or misuse of this project may violate applicable laws and regulations. The creators and OpenAI's GPT-3.5 model are not responsible for any misuse or illegal activities using this project.
