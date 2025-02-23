# Folder Encryption Using GPG 🚀

Welcome to the **Folder Encryption Using GPG** guide! This repository contains a step-by-step tutorial on how to securely encrypt and decrypt folders using **GPG (GNU Privacy Guard)** on Linux systems (including Ubuntu, RHEL, etc.).

## 🔑 Prerequisites

Before you start, ensure you have the following installed on your system:

- **GPG (GNU Privacy Guard)**: For encryption and decryption.
  - **For RHEL/CentOS**:  
    ```bash
    sudo dnf install gnupg
    ```
  - **For Ubuntu/Debian**:  
    ```bash
    sudo apt install gnupg
    ```

- **tar**: For creating compressed tar archives.

---

## 📝 Step-by-Step Guide

### 1️⃣ Convert Your Folder to a `.tar.gz` Archive

First, compress your folder into a `.tar.gz` file using the `tar` command:

```bash
tar -czvf file.tar.gz folder_name/
```
### 2️⃣ Create a GPG Key
To encrypt and decrypt files securely, generate a new GPG key:

```bash
gpg --full-generate-key
```
You will be prompted to select options:

* Key Type: Choose 1 (RSA and RSA).

* Key Size: Choose 4096 for higher security.

* Key Expiration: Type 0 for no expiration.

* Name & Email: Enter your details.

* Passphrase: Set a secure passphrase for your private key.

### 3️⃣ Encrypt the .tar.gz Archive
Once your key is created, encrypt the .tar.gz archive:

```bash
gpg --encrypt --recipient your_gmail@gmail.com --armor file.tar.gz
```
This generates an encrypted .asc file (file.tar.gz.asc), which is the securely encrypted version of your folder.

### 4️⃣ Decrypt the Encrypted File
To decrypt the .asc file, use:

```bash
gpg --output decrypted_file.tar.gz --decrypt file.tar.gz.asc
```
Enter your passphrase when prompted. This restores the original .tar.gz file.

### 5️⃣ Remove Saved Passphrase (Optional)
For extra security, clear the password cache:

```bash
gpgconf --kill gpg-agent
```
### ⚠️ Important: Secure Your Data
After encrypting your folder, it's recommended to delete the original unencrypted folder for security:

```bash
rm -rf folder_name/
```
Or securely wipe it:

```bash
shred -u -v folder_name/
```
For backup purposes, store the encrypted .asc file in:

An external encrypted drive
A secure cloud storage service

### ⚙️ Troubleshooting
Trust Issues
If asked about trust while creating or using a key, adjust the trust level:

```bash
gpg --edit-key your_gmail@gmail.com
```
Then type:

```bash
trust
```
Choose trust level 5 for "ultimate trust."

### ✨ Conclusion
By following these steps, you can securely encrypt and decrypt folders using GPG on Linux. This method ensures your sensitive data stays private and protected at all times! 🔐

If you have any issues or suggestions, feel free to reach out. Happy encrypting! 😊
