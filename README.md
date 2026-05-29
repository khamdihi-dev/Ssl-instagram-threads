# Instagram & Threads SSL Bypass (x86_64)

<p align="center">
  <img src="https://github.com/khamdihi-dev/Ssl-instagram-threads/blob/main/img/WhatsApp%20Image%202026-05-29%20at%2001.26.33.jpeg?raw=true" width="230"/>
  &nbsp;&nbsp;&nbsp;
  <img src="https://github.com/khamdihi-dev/Ssl-instagram-threads/blob/main/img/WhatsApp%20Image%202026-05-29%20at%2001.27.34.jpeg?raw=true" width="230"/>
</p>

<h3 align="center">
  SSL Pinning Bypass for Instagram & Threads Android
</h3>

<p align="center">
  Support latest Meta networking stack with Frida
</p>

---

## Supported Version

| Application | Version         | Architecture | Status    |
| ----------- | --------------- | ------------ | --------- |
| Instagram   | `430.0.0.53.80` | `x86_64`     | ✅ Working |
| Threads     | `430.0.0.46.79` | `x86_64`     | ✅ Working |

---

# Features

* SSL Pinning Bypass
* CertificateVerifier Hook
* TrustManager Bypass
* SSLContext Hook
* Meta Networking Hook
* Tigon / Proxygen Support
* Emulator Support
* Frida Compatible
* Native SSL Detection
* Cronet Detection

---

# Requirements

* Android Emulator `x86_64`
* Root Access
* Frida Server `x86_64`
* Python 3
* ADB
* Frida Tools

---

# Install Frida

```bash
pip install frida-tools
```

---

# Start Frida Server

Push frida-server:

```bash
adb push frida-server /data/local/tmp/
```

Run frida-server:

```bash
adb shell
su
chmod +x /data/local/tmp/frida-server
/data/local/tmp/frida-server &
```

---

# Verify Connection

```bash
frida-ps -U
```

---

# Usage

## Instagram

```bash
frida -U -f com.instagram.android -l ssl.js
```

## Threads

```bash
frida -U -f com.instagram.barcelona -l ssl.js
```

---

# Hooks Included

* TrustManagerImpl
* SSLContext.init
* CertificateVerifier
* Native SSL Detection
* Tigon Detection
* Proxygen Detection
* Cronet Detection

---

# Notes

* Tested on Android Emulator `x86_64`
* Recommended Android 10+
* Some builds may require QUIC disable
* Use matching frida-server architecture

---

# Contact

Need private bypass, latest update, or support?

<p align="center">
  <a href="https://wa.me/6283853140469">
    <img src="https://img.shields.io/badge/WhatsApp-Contact-green?style=for-the-badge&logo=whatsapp"/>
  </a>
</p>

---

# Disclaimer

This project is intended for educational and security research purposes only.
