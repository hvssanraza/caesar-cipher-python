Caesar Cipher in Python

A simple Python implementation of the Caesar Cipher, one of the oldest and most famous classical cryptographic techniques.
This project demonstrates encryption, decryption, and brute-force attacks on Caesar Cipher, making it a great starting point for learning about classical cryptography.

🔑 Features

Encryption – Shift plaintext letters by a chosen key.

Decryption – Reverse the process using the same key.

Brute-force Attack – Try all 26 possible shifts to recover the plaintext when the key is unknown.

Handles both uppercase and lowercase letters.

Preserves spaces and punctuation.

🧮 How the Caesar Cipher Works

Each letter in the plaintext is shifted by a fixed number (key) down the alphabet.

Formulae:

Encryption: C = (P + k) mod 26

Decryption: P = (C - k) mod 26

Example with shift = 3:

Plaintext : HELLO
Ciphertext: KHOOR

🚀 Getting Started
Prerequisites

Python 3.6+

Running the Program

Clone the repository:

git clone https://github.com/your-username/caesar-cipher-python.git
cd caesar-cipher-python


Run the program:

python caesar_cipher.py

💻 Example Usage
1. Encryption
Enter message: Hello i am Hassan Raza
Enter shift value: 1
Encrypted message: Ifmmp j bn Ibttbo Sbab

2. Decryption
Enter encrypted message: Ifmmp j bn Ibttbo Sbab
Enter shift value: 1
Decrypted message: Hello i am Hassan Raza

3. Brute-Force Attack
Enter encrypted text: Ifmmp j bn Ibttbo Sbab

shift  1: Hello i am Hassan Raza  <-- correct
shift  2: Gdkkn h zl Gzrrzm Qzyz
shift  3: Fcjjm g yk Fyqqyl Pyxy
...

📂 Project Structure
.
├── caesar_cipher.py   # Main script (encryption, decryption, brute force)
├── README.md          # Documentation

📖 Future Improvements

Add support for other classical ciphers (Vigenère, Atbash, etc.)

Extend with frequency analysis attack.

Build a simple GUI or web version for demonstration.

📜 License

This project is licensed under the MIT License – feel free to use and modify for learning purposes.
