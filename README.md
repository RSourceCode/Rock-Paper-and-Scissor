# ✊✋✌️ Rock Paper Scissors – Network Multiplayer Game

A multiplayer **Rock-Paper-Scissors** game built with **Python**, using **Pygame** for the interface and **sockets** for real-time two-player communication over a network.

---

## 🎮 Features

* Real-time **2-player online gameplay**
* Uses **sockets** and **multithreading** to handle multiple clients
* Friendly **graphical interface** using Pygame
* Includes **move lock-in**, **score tracking**, and **winner display**
* Simple and extendable **server-client architecture**

---

## 🧱 Architecture

This game uses a **Client-Server** model:

```
        [Player 1] <--->  |           |
                          |  Server   |
        [Player 2] <--->  |           |
```

* The server hosts the game state and synchronizes both players.
* Each client connects and sends their move to the server.
* Server evaluates the winner and resets the game state.

---

## 🗃️ Project Structure

```
rock-paper-scissors-network/
│
├── client.py           # Main client interface (Pygame UI)
├── game.py             # Game logic (winner, state, moves)
├── network.py          # Client-side socket communication
├── server.py           # Server-side socket handling
└── README.md           # Documentation
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/rock-paper-scissors-network.git
cd rock-paper-scissors-network
```

### 2. Install dependencies

Ensure Python 3 is installed.

```bash
pip install pygame
```

### 3. Run the server (on host machine)

```bash
python server.py
```

### 4. Run the client (on each player’s machine)

Make sure `network.py` points to the correct server IP.

```python
# in network.py
self.server = "YOUR_SERVER_IP"  # Replace with actual IP
```

Then run:

```bash
python client.py
```

---

## 🕹️ How to Play

0. Server must be running.
1. Both players run the client script.
2. Click on one of the buttons: **Rock**, **Paper**, or **Scissors**.
3. Once both players choose, the result is shown:

   * 🟦 *You Won!*
   * 🟥 *You Lost...*
   * ⚪ *Tie Game!*
4. The round resets automatically.

---

## 🌐 Network Configuration

* Default port: `5555`
* Ensure port is open on the host machine.
* You can host the server locally.
---

---

Let me know if you want a matching image/gif preview, or if you'd like me to create a GitHub-friendly version with markdown file or code comments too!
