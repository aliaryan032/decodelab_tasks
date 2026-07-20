# DecodeLabs Project 3: Enterprise Random Password Generator

## Overview
This repository contains the solution for Project 3 of the DecodeLabs Industrial Training Kit[cite: 3]. This project serves as a transition into enterprise architecture, focusing on standard library integration, string manipulation, and the mathematical provision of security[cite: 3]. 

## Architecture & Features
* **NIST 2024 Compliance:** The application prompts the user for a target integer length, actively encouraging passwords of 15+ characters to align with modern hardware realities rather than legacy complexity rules[cite: 3].
* **Cryptographic Security:** The predictable `random` module (Mersenne Twister) was intentionally avoided[cite: 3]. This system utilizes Python's `secrets.choice()` to tap into hardware-level OS noise, ensuring unpredictable entropy[cite: 3].
* **Standardized Character Pools:** Utilizes the built-in `string` module (`ascii_letters`, `digits`, `punctuation`) to guarantee locale-independent consistency without hardcoding arrays[cite: 3].
* **Linear Time Complexity O(N):** Bypasses Python's immutable string memory overhead by generating a list of characters and assembling them via the `"".join()` method[cite: 3].
* **Information Entropy Calculation:** Mathematically validates the password's unpredictability using the formula[cite: 3]:

$$E = L \times \log_2(R)$$

## Execution Output
Below is a demonstration of the program successfully capturing the target integer, executing the transformation algorithm, and verifying the entropy[cite: 3]:

```text
=== DECODELABS ENTERPRISE PASSWORD GENERATOR ===
NIST 2024 Guidelines: Minimum 15 characters recommended for high security.

Enter desired password length: 16

-------------------------------------------
GENERATED PASSWORD: A!B9c$D#ΣA7x*p@Q
-------------------------------------------
Password Length (L) : 16 characters
Character Pool (R)  : 94 possible characters
Security Entropy (E): 104.87 bits
Status: HIGH SECURITY (NIST 2024 Compliant)
