# Secure Steganography & Encryption Tool

## Overview
In cybersecurity, encryption hides *what* you are saying, but steganography hides the fact that you are saying *anything at all*.

This project implements a dual-layer security approach to digital privacy:
1.  **Cryptography:** Locks sensitive text messages using **AES-128 encryption**, ensuring that even if the data is intercepted, it cannot be read without a key.
2.  **Steganography:** Uses **Least Significant Bit (LSB)** manipulation to embed that encrypted payload directly into the pixels of an image file.

The result is a standard-looking image that secretly carries a locked message—demonstrating how secure communication channels can be established in surveillance-heavy environments.

## Key Features
* **Dual-Layer Security:** Combines AES encryption with LSB image hiding.
* **Pixel-Level Manipulation:** Manually processes image binary data using `PIL` (Pillow).
* **Automated Pipeline:** Functions to encode, decode, and verify data integrity in one step.
* **Robustness Testing:** Includes scripts to test payload capacity and encryption speed.

## Tech Stack
* **Language:** Python 3.x
* **Cryptography:** `pycryptodome` (AES-128, ECB Mode, PKCS7 Padding)
* **Image Processing:** `Pillow` (PIL)
* **Visualization:** `matplotlib`

## How to Run
1.  **Install Dependencies:**
    ```bash
    pip install pycryptodome pillow matplotlib numpy cryptosteganography
    ```

2.  **Run the Script:**
    Update the `image_path` variable in `crypto.py` to point to your image, then run:
    ```bash
    python crypto.py
    ```

## Educational Note
This tool uses **AES-ECB** mode for demonstration purposes. For production-grade security, it is recommended to switch to **AES-GCM** or **CBC** to prevent pattern leakage.
