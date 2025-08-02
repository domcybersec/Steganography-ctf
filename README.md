# 🕵️‍♂️ Steganography CTF Project

This project is a custom steganography-based capture-the-flag (CTF) challenge designed to demonstrate basic cryptography, hashing, and steganographic techniques. Three image files contain embedded and encrypted clues that must be extracted and decrypted in sequence to reach the final solution.

---

## 📁 Project Structure

| File Name      | Description                                     |
|----------------|-------------------------------------------------|
| `SecPlus1.png` | Block 1 — Encodes a Base64 challenge       |
| `SecPlus2.png` | Block 2 — Requires the key revealed in Block 1  |
| `SecPlus3.png` | Block 3 — Final encrypted clue                  |

---

## 🛠 Tools Used

- [OpenStego](https://www.openstego.com) — for hiding and extracting data in images
- `sha3256` — for hashing strings
- `echo` — to generate hash inputs
- CyberChef - to get output from hash and base64
- Linux Terminal — for file handling and command-line utilities

---

## 🔓 How to Extract the Hidden Messages

> You must use [OpenStego](https://www.openstego.com) and the correct password for each block.

### 🧩 Block 1 — Base64 String
- Extract the message from `SecPlus1.png`
- Your task is to use the phrase "Start Here" to recover a base64 string
- Decode the string to get a phrase that can then be used in the next block.

### 🧩 Block 2 — Hashing and Key Generation 
- Use the correct input from Block 1 as the password
- Extract the embedded message from `SecPlus2.png`
- Use the text to create a Sha-3-256 hash

### 🧩 Block 3 — Final Message
- Using the pass phrase taken from image #2 you will get an encrypted file from image #3. 
- Using the hash created from the embeded phrase in the last block as a symetric key decrypt the file
- Gather the flag

Extract hidden data:

✍️ Author

Dom Waters
GitHub: @domcybersec
CTF/Infosec Enthusiast & Cybersecurity Student
