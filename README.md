# 🔐 Encryption for Dummies

Welcome to my repository!  
Here, I explore and explain various **encryption techniques**, including classical ciphers like the **Vigenère cipher**, **Caesar cipher**, and more.

> ⚠️ **Work in Progress**  
> This project is actively being developed and updated frequently. New content and improvements are added regularly, stay tuned!

Feel free to browse the examples, follow the logic, and dive into how these algorithms work step by step.

---

## 📑 Index

- [Vigenère Cipher](#vigenère-cipher)
  - [Alphabet Indexing (0–25)](#alphabet-indexing-025)
  - [🔐 Encryption Example](#-encryption-example)

---

# Vigenère Cipher

The **Vigenère cipher** is a method of encrypting alphabetic text where each letter of the plaintext is encoded using a Caesar cipher. The shift for each letter is determined by the corresponding letter of a keyword (the key).

---

## Alphabet Indexing (0–25)

Each letter of the alphabet is assigned a numerical value:

| Letter | Value | Letter | Value | Letter | Value | Letter | Value |
|--------|-------|--------|-------|--------|-------|--------|-------|
| A      | 0     | G      | 6     | M      | 12    | S      | 18    |
| B      | 1     | H      | 7     | N      | 13    | T      | 19    |
| C      | 2     | I      | 8     | O      | 14    | U      | 20    |
| D      | 3     | J      | 9     | P      | 15    | V      | 21    |
| E      | 4     | K      | 10    | Q      | 16    | W      | 22    |
| F      | 5     | L      | 11    | R      | 17    | X      | 23    |
|        |       |        |       |        |       | Y      | 24    |
|        |       |        |       |        |       | Z      | 25    |

---

## 🔐 Encryption Example

You want to encrypt the plaintext `"DUCK"` using the key `"WOLF"`.

### Input
- **Plaintext**: `DUCK`
- **Key**: `WOLF`

### Output
- **Encrypted Text**: `ZJNP`

### Step-by-Step Logic

| Plaintext | Key | P (value) | K (value) | (P + K) mod 26 | Result |
|-----------|-----|-----------|-----------|----------------|--------|
| D         | W   | 3         | 22        | 25             | Z      |
| U         | O   | 20        | 14        | 8              | J      |
| C         | L   | 2         | 11        | 13             | N      |
| K         | F   | 10        | 5         | 15             | P      |

> Encryption formula:  
> **Encrypted letter** = (Plaintext letter value + Key letter value) mod 26

---
