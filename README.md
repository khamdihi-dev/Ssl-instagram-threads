# Instagram & Threads SSL Bypass (x86_64)

Support terbaru untuk:

* Instagram `430.0.0.53.80`
* Threads `430.0.0.46.79`

Architecture:

```txt id="i34kb7"
x86_64
```

## Features

* SSL Pinning Bypass
* CertificateVerifier Hook
* TrustManager Bypass
* SSLContext Hook
* Meta Networking Hook
* Tigon / Proxygen Support
* Emulator Support
* Frida Compatible

## Supported Apps

| App       | Version       | Architecture | Status    |
| --------- | ------------- | ------------ | --------- |
| Instagram | 430.0.0.53.80 | x86_64       | ✅ Working |
| Threads   | 430.0.0.46.79 | x86_64       | ✅ Working |

## Requirements

* Android Emulator x86_64
* Root Access
* Frida Server x86_64
* Frida Tools
* Python 3
* ADB

## Install Frida

```bash id="ux54r5"
pip install frida-tools
```

## Start Frida Server

Push frida-server:

```bash id="76gdz7"
adb push frida-server /data/local/tmp/
```

Run:

```bash id="lpjlwm"
adb shell
su
chmod +x /data/local/tmp/frida-server
/data/local/tmp/frida-server &
```

## Verify Connection

```bash id="6o74m2"
frida-ps -U
```

## Usage

Instagram:

```bash id="jlwm7d"
frida -U -f com.instagram.android -l ssl.js
```

Threads:

```bash id="39kquu"
frida -U -f com.instagram.barcelona -l ssl.js
```

## Hooks Included

* TrustManagerImpl
* SSLContext.init
* CertificateVerifier
* Native SSL Detection
* Tigon Detection
* Proxygen Detection
* Cronet Detection

## Notes

* Tested on Android Emulator x86_64
* Recommended Android 10+
* Some builds may require QUIC disable
* Use matching frida-server architecture

## Contact

Need private bypass / latest update / support?

WhatsApp:

```txt id="jlwmk7"
+6283853140469
```

## Disclaimer

For educational and security research purposes only.
