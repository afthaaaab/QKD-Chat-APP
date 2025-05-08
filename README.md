# QKD-Chat-APP
Secure chat application implementing the BB84 Quantum Key Distribution (QKD) protocol for end-to-end encrypted communication.

# 🔐 QKD Secure Chat App

A secure peer-to-peer chat application that implements the **BB84 Quantum Key Distribution (QKD)** protocol for **end-to-end encrypted communication**. This project simulates quantum key exchange using BB84 and leverages AES encryption to ensure secure message transmission between two clients.

---

## 📌 Features

- 🔑 Simulated BB84 Quantum Key Distribution (QKD)
- 🧪 Eavesdropping detection during key exchange
- 🔐 AES symmetric encryption with quantum-generated key
- 💬 Real-time chat between two users
- 🛠️ Simple CLI interface for educational use

---
## 🔐 Why AES if we have QKD?

**QKD provides a secure key exchange**—not encryption. Once the key is shared securely using QKD, 
**AES (or any symmetric cipher)** is used to encrypt the actual messages. 
QKD just ensures the key was never intercepted or tampered with.

---

## 🧪 How to Use

1. Both users unzip and run the script.
2. One user selects `host`, the other selects `client` and inputs the IP of the host.
3. Chat securely after QKD key generation.

---

## ⚙️ The Only Requirement

pip install pycryptodome

---

## ⚙️ Setup & Installation

### 🛑 Prerequisites

- Python 3.8 or higher
- `pip` package manager

### 🛠️ Install Dependencies

git clone https://github.com/afthaaaab/QKD-Chat-APP.git
cd qkd-chat-app
pip install pycryptodome


## 🧠 How It Works

### 🔸 BB84 Protocol

The BB84 protocol simulates quantum key generation using randomly selected bases (rectilinear `+` and diagonal `×`) to encode and decode bits.

1. **Alice** (Sender) generates a random bit string and basis string.
2. **Bob** (Receiver) independently selects random bases.
3. Bob measures the qubits based on his bases.
4. Both compare their basis choices over a public channel.
5. Bits with matching bases are retained to form the **raw key**.
6. A subset of the key is publicly compared to check for eavesdropping.
7. If the test passes, the remaining bits are used as the **secret key**.

### 🔸 Secure Chat

- The secret key is used as the AES key for symmetric encryption.
- Chat messages are encrypted and decrypted using this key.
- The server only routes encrypted data — it cannot read the contents.

###🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change or enhance (e.g., GUI version, advanced QKD model, error correction).

###📚 References
Bennett, C. H., & Brassard, G. (1984). "Quantum cryptography: Public key distribution and coin tossing" (BB84 Protocol).

Quantum Key Distribution – IBM Quantum Docs

PyCryptodome – AES implementation in Python


