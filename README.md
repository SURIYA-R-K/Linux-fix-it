# Linux Encryption and Decryption with GPG

This repository provides a step-by-step guide on how to encrypt and decrypt files or folders using GPG (GNU Privacy Guard) on Linux systems. It will also cover troubleshooting steps for common issues you may encounter during encryption and decryption processes.

## Table of Contents
- [Encrypting a Folder](#encrypting-a-folder)
- [Creating a GPG Key](#creating-a-gpg-key)
- [Encrypting a File with GPG](#encrypting-a-file-with-gpg)
- [Decrypting a File with GPG](#decrypting-a-file-with-gpg)
- [Troubleshooting](#troubleshooting)

## Encrypting a Folder

To encrypt a folder, follow these steps:

1. **Convert the folder into a tar.gz file**:

   ```bash
   tar -cvf file.tar.gz file/
This command will convert the folder into a tar file.

Creating a GPG Key
Generate a GPG key:

bash
Copy
gpg --full-generate-key
Choose the following options:

Type: Select 1 (RSA and RSA).
Key size: Choose 4096 for enhanced security.
Duration: Set the key to expire or choose 0 for no expiration.
User Information: Provide your name, email address, and a comment (optional).
Encrypting a File with GPG
Encrypt the tar file:

bash
Copy
gpg --encrypt --recipient your_gmail@gmail.com --armor file.tar.gz
This will encrypt the file and create a .asc encrypted file.

Decrypting a File with GPG
Decrypt the encrypted file:

bash
Copy
gpg --output decrypted_file.tar.gz --decrypt file.tar.gz.asc
After providing the password for the GPG key, the file will be decrypted.

Clear saved password (optional):

If you want to remove the saved password from the keyring, use the following command:

bash
Copy
gpgconf --kill gpg-agent
Troubleshooting
Trust Issues: If you're asked about trust while creating or using a key, you can adjust the trust settings using the following command:

bash
Copy
gpg --edit-key your_gmail@gmail.com
Then, type:

bash
Copy
trust
Select the trust level (usually 5 for ultimate trust).

Trust Model Warning: If you encounter the warning marginals needed: 3 completes needed: 1 trust model: pgp, it means that the key's trust hasn't been fully verified. You may need to manually trust the key or import a trusted key.

By following these steps, you can securely encrypt and decrypt your files or folders on Linux systems using GPG.

sql
Copy

Simply copy and paste this into the `README.md` file of your GitHub repository. Let me know if you need any further adjustments!
