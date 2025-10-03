# Caesar Cipher in Python

A clean, professional implementation of the **Caesar Cipher** demonstrating encryption, decryption, and brute-force attacks.  
Designed for learning and easy extension to other classical ciphers.

---

## Features
- **Encryption** — shift plaintext by a chosen key.  
- **Decryption** — recover plaintext using the same key.  
- **Brute-force attack** — try all 26 shifts to recover plaintext when the key is unknown.  
- Preserves **case**, and leaves spaces & punctuation unchanged.  
- Small, readable, and easy to extend.

---

## Quick Start

### Prerequisites
- Python 3.6 or later

### Clone & Run
```bash
git clone https://github.com/hvssanraza/caesar-cipher-python.git
cd caesar-cipher-python
python caesar-cipher-python.py
```

---

## Usage

### Encryption
```
Enter message: Hello i am Hassan Raza
Enter shift value: 1
Encrypted message: Ifmmp j bn Ibttbo Sbab
```

### Decryption
```
Enter encrypted message: Ifmmp j bn Ibttbo Sbab
Enter shift value: 1
Decrypted message: Hello i am Hassan Raza
```

### Brute-force Attack
```
Enter encrypted text: Ifmmp j bn Ibttbo Sbab

shift  1: Hello i am Hassan Raza  <-- likely valid
shift  2: Gdkkn h zl Gzrrzm Qzyz
shift  3: Fcjjm g yk Fyqqyl Pyxy
...
```

---

## Implementation Notes
- The code maps letters to a 0–25 index using their ASCII codes:
  - Uppercase base = `ord('A') = 65`
  - Lowercase base = `ord('a') = 97`
- Shift formula used for encryption:
  ```
  encrypted_char = chr((ord(char) - base + shift) % 26 + base)
  ```
  Decryption is the same with `-shift` (or `26 - (shift % 26)`).
- Non-alphabetic characters are copied unchanged.

---

## Project Structure
```
.
├── caesar-cipher-python.py   # Main script: encryption, decryption, brute-force
├── README.md          # This file
```

---

## Example `caesar_cipher.py` (recommended)
```python
def caesar_shift(text, shift):
    out = []
    for ch in text:
        if ch.isalpha():
            base = ord('A') if ch.isupper() else ord('a')
            out.append(chr((ord(ch) - base + shift) % 26 + base))
        else:
            out.append(ch)
    return ''.join(out)

def encrypt():
    text = input("Enter message: ")
    shift = int(input("Enter shift value: "))
    print("Encrypted message:", caesar_shift(text, shift))

def decrypt():
    cipher = input("Enter encrypted message: ")
    shift = int(input("Enter shift value: "))
    print("Decrypted message:", caesar_shift(cipher, -shift))

def brute_force():
    cipher = input("Enter encrypted text: ")
    for s in range(1, 27):
        print(f"shift {s:2d}: {caesar_shift(cipher, -s)}")

def main():
    menu = ("1) Encrypt\n2) Decrypt\n3) Brute-force attack\n4) Exit\nChoose: ")
    while True:
        choice = input(menu).strip()
        if choice == '1': encrypt()
        elif choice == '2': decrypt()
        elif choice == '3': brute_force()
        elif choice == '4': break
        else: print("Invalid choice")

if __name__ == "__main__":
    main()
```

---

## Future Improvements
- Add other classical ciphers (Vigenère, Atbash, etc.).  
- Implement frequency analysis for automated key detection.  
- Provide unit tests and CLI flags for automation.  
- Build a simple GUI or web front-end for demonstrations.

---
