# 🖥️ Terminal Messaging - UDP Chatbot with AI Integration

**Terminal Messaging** is a multi-client, multi-server UDP-based chatbot system enhanced with **OpenAI ChatGPT AI** developed by our group consisting of Yusif Malikov, Michael Lima, and Dimitri Kovzanadze. This project allows clients to communicate seamlessly across servers, run AI-powered chatbots, and utilize terminal commands for advanced networking features.

---

## 🌐 Features

| Feature                                     | Description                                                                                                                                  |
| ------------------------------------------- | ------------------------------------------------------------------
| **OpenAI Integration**                      | Each server can run `robot.py` to provide AI responses. Users can chat with the AI as if it were a regular participant.                      |
| **Quit Chat `!q`**                          | Safely exit the chat. Sends a “left the chat” message to the server before closing the client.                                               |
| **Ping Command `/ping <ip>`**               | Check if a specific IP is reachable via ICMP ping. Runs locally and does not broadcast messages to the server.                               |
| **Join Another Server `/join <server_ip>`** | Switch to a different server by updating the destination IP. Server sends a “JOINED THE SERVER” notification to the client.                     |

---

## 🛠️ Terminal Commands

| Command             | Usage               | Description                                                                |
| ------------------- | ------------------- | -------------------------------------------------------------------------- |
| `!q`                | `!q`                | Exit the chat safely. Sends a notification to the server.                  |
| `/ping <ip>`        | `/ping 192.168.0.1` | Ping a specific IP locally to check reachability.                          |
| `/join <server_ip>` | `/join 192.168.0.2` | Switch to a different server and notify the new server about your arrival. |

---

## 🤖 AI Integration

Each server can run `robot.py` to handle AI responses:

* The AI acts as a chat participant.
* Clients can send messages directly to the AI.
* Responses are returned instantly via the server.

---

## 📡 Demo Topology

The following diagram illustrates the network setup used in our class demo:

![ChatGPT Image Dec 16, 2025, 01\_03\_22 PM](https://github.com/user-attachments/assets/5b68f702-c6d7-409c-a2cb-fecd0b6700ca)

* **IP Assignments:** Same as class demo.
* **Network Flow:** Clients can chat, run `/ping`, or switch servers with `/join`. AI responses are handled by `robot.py` running on servers.

---

## 🚀 Getting Started

1. **Run a server:**

   ```bash
   python server.py
   ```
2. **Start a client:**

   ```bash
   python client.py
   ```
3. **Optional:** Start AI on the server:

   ```bash
   python robot.py
   ```
4. **Use commands in the client:**

   * Quit: `!q`
   * Ping: `/ping <ip>`
   * Join server: `/join <server_ip>`

THANK YOU FOR YOUR ATTENTION AND ENJOY!
