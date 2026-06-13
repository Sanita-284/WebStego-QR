# WebStegoQR 🔐

A web-based steganographic QR code encryption system that combines **AES-256-CBC cryptography** with **QR code steganography** to securely hide and transfer sensitive data.

> B.Tech Project — Department of Computer Science & Engineering, Jain Deemed to be University (March 2025)

## 🔗 Demo Link

🌐 **Live Application:** https://your-demo-url.com

---

## 📌 Overview

WebStegoQR lets users encrypt a message using a secret key, embed the encrypted data into a QR code, and later decrypt it by scanning the QR code and providing the same key. Even if an attacker obtains the QR code, decryption is impossible without the correct key.

---

## ✨ Features

- 🔒 **AES-256-CBC encryption** with PKCS7 padding
- 🎲 **Random IV generation** — unique encrypted output every time, even for identical messages
- 📷 **QR code generation & decoding** — encrypted data embedded directly into a scannable QR
- 🚫 **No key storage** — keys are never saved server-side, minimizing breach exposure
- 🌐 **Fully web-based** — works in any modern browser
- 🎨 **Cyberpunk-themed UI** built with HTML, CSS, Bootstrap, and JavaScript

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML, CSS, JavaScript, Bootstrap |
| Backend | Python, Flask, Gunicorn |
| Encryption | PyCryptodome (AES-CBC) |
| QR Code | `qrcode`, `Pillow (PIL)`, `jsQR` |
| Image Processing | OpenCV |
| Hosting | Render |
| Version Control | GitHub |

---

## ⚙️ How It Works

### Encryption

1. User enters text and an 8-character key
2. Key is padded to meet AES-256 requirements
3. A random 16-byte IV is generated
4. Text is encrypted using AES-CBC mode
5. Encrypted data is encoded into a QR code
6. QR code is displayed for download or sharing

### Decryption

1. User uploads a QR code image and provides the key
2. System scans and extracts the encrypted data from the QR code
3. AES-CBC decrypts the data using the provided key
4. Original text is displayed — or an error shown if the key is wrong

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- pip

### Installation

```bash
git clone https://github.com/your-username/WebStegoQR.git
cd WebStegoQR
pip install -r requirements.txt
python app.py
```

Then open your browser at:

```text
http://localhost:5000
```

### Requirements (`requirements.txt`)

```txt
flask
pycryptodome
qrcode[pil]
pillow
opencv-python
gunicorn
```

---

## 📁 Project Structure

```text
WebStegoQR/
├── app.py
├── templates/
│   └── indexqr.html
├── static/
│   ├── css/
│   ├── js/
│   └── images/
├── requirements.txt
└── README.md
```

---

## 🔐 Security Design

- AES-CBC mode prevents pattern-based attacks on ciphertext
- Random IV ensures no two encryptions of the same message look alike
- Keys are never stored server-side
- HTTPS protects data in transit
- Tampered QR codes become unreadable, acting as implicit tamper detection

---

## 📊 Performance

| Metric | Result |
|----------|---------|
| Avg. Encryption Time | ~0.5 seconds |
| Avg. Decryption Time | ~0.6 seconds |
| QR Code Generation | ~0.3 seconds |
| QR Scanning Accuracy | 99.8% |
| Decryption Accuracy (Correct Key) | 100% |

---

## 🔭 Future Improvements

- [ ] AES-GCM for authenticated encryption
- [ ] Hybrid Encryption (AES + RSA)
- [ ] Segmented QR support for large messages
- [ ] Android & iOS applications
- [ ] Blockchain-based decentralized storage
- [ ] Multi-factor authentication

---

## 💡 Applications

- Secure peer-to-peer messaging
- Banking OTP protection
- Healthcare record security
- Digital document authentication
- Cybersecurity credential sharing

---

## 👥 Authors

| Name | Roll Number |
|--------|------------|
| Monica P | 23BTRCC027 |
| Sanita | 23BTRCC034 |
| Vaishnavi S | 23BTRCC039 |
| Vinotha M | 23BTRCC044 |
| Surya Vignesh | 23BTRCC051 |

**Project Guide:** Mr. Adarsh Tiwari  
Department of Computer Science & Engineering  
Jain Deemed to be University

---

## 📚 References

1. Alajmi et al. — *Steganography of Encrypted Messages Inside Valid QR Codes* (IEEE, 2020)
2. Mendhe et al. — *Secure QR-Code Based Message Sharing System* (IEEE, 2019)
3. Lin & Chen — *QR Code Steganography with Secret Payload Enhancement* (IEEE, 2016)
4. Mittal et al. — *Privacy and Security Using QR-Code through Homomorphic Encryption* (IEEE, 2021)
5. Karthikeyan et al. — *Enhanced Security in Steganography Using QR Code* (IEEE, 2016)
6. Prasad & Pramod — *QR DWT Guided Steganography Using Machine Learning* (IEEE, 2024)
7. Sun et al. — *QR Code Steganography Based on JSteg Algorithm in DCT Domain* (IEEE, 2020)

---

## 📄 License

This project was developed for academic purposes as part of the B.Tech degree program.

Feel free to use, modify, and extend this project with proper attribution to the authors.

---

> 🔐 Secure Messages. Scannable Delivery. Zero Key Storage.
