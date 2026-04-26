# 🚀 Single-threaded HTTP Web Server in C++

Created by **Deepak Singh**
**3rd Year | CSE | NIT Jalandhar**

This is a single-threaded HTTP web server built entirely from scratch using **C++** and low-level **Linux socket programming**. It handles raw HTTP requests, parses them manually, and responds with HTML or plain text — all without using any external libraries or frameworks.

---

## 🌟 Features

* ✅ Manual socket creation, binding, listening, and accepting
* ✅ Parses raw HTTP GET requests
* ✅ Single-threaded server architecture
* ✅ Clean object-oriented architecture
* ✅ Serves static HTML files or plain text responses
* ✅ 100% written in C++ with no external dependencies

---

## 🔧 Requirements

Works on any Linux system with `g++` installed.

Install g++ if not already installed:

```bash
sudo apt update
sudo apt install g++
```

---

## 🧩 Project Structure

```text
.
├── Networking/
│   ├── simplesocket.hpp / cpp       # Base socket class (create socket, test connection)
│   ├── bindingsocket.hpp / cpp      # Adds bind() functionality
│   ├── connectingsocket.hpp / cpp   # Adds connect() (for client-side use)
│   ├── listeningsocket.hpp / cpp    # Adds listen() for server-side
│   ├── simpleserver.hpp / cpp       # Abstract class for a server
│   ├── testserver.hpp / cpp         # Final server logic
│   ├── test.cpp                     # Entry point to run the server
│   ├── main.cpp                     # Optional testing file
│   └── index.html                   # Optional static HTML file
└── README.md
```

---

## ⚙️ How It Works

The server uses the following Linux system calls:

* `socket()`
* `bind()`
* `listen()`
* `accept()`
* `read()`
* `write()`
* `close()`

Flow:

1. Creates a socket
2. Binds it to `localhost:3000`
3. Starts listening for browser requests
4. Accepts incoming client connections
5. Reads raw HTTP requests
6. Sends HTTP response back to browser
7. Closes the connection

---

## 🚀 Running on Linux

### 1. Clone the Project

```bash
git clone https://github.com/DEEPAKSINGH275/CPP-Http-web-server-Single-thread-for-Linux.git
cd CPP-Http-web-server-Single-thread-for-Linux
```

---

### 2. Move to Networking Folder

```bash
cd Networking
```

---

### 3. Compile the Project

```bash
g++ -std=c++17 -pthread -o server \
test.cpp \
testserver.cpp \
simpleserver.cpp \
listeningsocket.cpp \
bindingsocket.cpp \
connectingsocket.cpp \
simplesocket.cpp
```

---

### 4. Run the Server

```bash
./server
```

You will see:

```bash
---waiting---
http://localhost:3000
```

---

### 5. Open in Browser

Go to:

```bash
http://localhost:3000
```

or

```bash
http://127.0.0.1:3000
```
<img width="1717" height="689" alt="project_preview.png" src="https://github.com/user-attachments/assets/378a132d-c2d0-411a-80e5-fd8068909e66" />
---

## 🧠 Learning Outcomes

This project teaches:

* Socket programming in C++
* How HTTP actually works (manual request parsing)
* Linux networking fundamentals
* Building backend infrastructure from scratch
* Clean OOP design and class architecture
* TCP/IP communication using sockets

---

## 👨‍💻 Made By

**Deepak Singh**
3rd Year, Computer Science and Engineering
NIT Jalandhar, India
