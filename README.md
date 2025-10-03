🔐 Caesar Cipher in Python

A clean, professional implementation of the Caesar Cipher demonstrating encryption 🔒, decryption 🔓, and brute-force attacks 🛠️.
Designed for learning 📘 and easy extension to other classical ciphers.

✨ Features

🔒 Encryption — shift plaintext by a chosen key

🔓 Decryption — recover plaintext using the same key

🛠️ Brute-force attack — try all 26 shifts when the key is unknown

📝 Preserves case, spaces, and punctuation

📜 Small, readable, and easy to extend

🚀 Quick Start
✅ Prerequisites

Python 3.6 or later

📂 Clone & Run
git clone https://github.com/hvssanraza/caesar-cipher-python.git
cd caesar-cipher-python
python caesar-cipher-python.py

🖥️ Usage
🔒 Encryption
Enter message: Hello i am Hassan Raza
Enter shift value: 1
Encrypted message: Ifmmp j bn Ibttbo Sbab

🔓 Decryption
Enter encrypted message: Ifmmp j bn Ibttbo Sbab
Enter shift value: 1
Decrypted message: Hello i am Hassan Raza

🛠️ Brute-force Attack
Enter encrypted text: Ifmmp j bn Ibttbo Sbab

shift  1: Hello i am Hassan Raza  <-- likely valid
shift  2: Gdkkn h zl Gzrrzm Qzyz
shift  3: Fcjjm g yk Fyqqyl Pyxy
...

🛠️ Implementation Notes

Uses ASCII mapping:

ord('A') = 65 for uppercase

ord('a') = 97 for lowercase

Formula for shift:

encrypted_char = chr((ord(char) - base + shift) % 26 + base)


Non-alphabetic characters remain unchanged ✅

📂 Project Structure
.
├── caesar-cipher-python.py   # Main script: encryption, decryption, brute-force
├── README.md                 # Documentation

📌 Future Improvements

🔑 Add more classical ciphers (Vigenère, Atbash, etc.)

📊 Implement frequency analysis for auto key detection

🧪 Unit tests & CLI flags for automation

🌐 GUI or web front-end for demos

👨‍💻 Author

Hassan Raza ✨
🎓 BS Artificial Intelligence
🔐 Security & AI Enthusiast
🚀 Exploring innovative tech solutions
