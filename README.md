# ⚡ Zam! (Zero-Knowledge File Buffer)

Zam is a lightning-fast, zero-knowledge CLI and Web tool for securely sharing files and folders. 

It locally compresses and encrypts your data using **AES-256-GCM** (with PBKDF2 Key Derivation) *before* it leaves your machine. The server is mathematically blind to your data, and everything self-destructs after exactly 48 hours.

🌐 **Web Interface:** [zam.ftp.sh](https://zam.ftp.sh)

## 📥 Installation

Download the latest version for your operating system from the [Releases Page](../../releases/latest).

### Linux / macOS
```bash
# Move it to your path to run it globally
chmod +x zam-linux-amd64
sudo mv zam-linux-amd64 /usr/local/bin/zam
```
---
# 📖 How to Use
## Sending Files & Folders
```bash
zam up <file_or_folder>
```
It will ask you to set a secret key. It will then automatically compress, encrypt, and upload the payload, returning a short-link.

# Receiving Files

```bash
zam down <url_or_id>
```
It will ask for the secret key, decrypt the payload, and restore your original file/folder.

# 💡 Clever Ways to Use Zam

- The Secure Dead Drop: Share sensitive keys or documents anonymously. Zam leaves no server logs and requires no accounts.

- The DevOps Secret Handshake: Stop pasting .env files or SSH keys into Slack or Discord where they live forever. Zam them instead.

Built with ⚡ by Vibhor Shukla.
