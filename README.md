# Project Structure to check repo Ownership
```plaintext
repository-verification/
├── README.md           # Contains the public key and instructions
├── public_key.pem      # Public key in PEM format
├── signature.bin       # Cryptographic signature of the message
├── message.txt         # Original message that was signed
```
## Details of Each File
### 1. `README.md`
Have to include public_key.
```plaintext
# Repository Ownership Verification

This repository includes cryptographic proof of ownership. The files in this repository allow anyone to verify that the repository owner controls the private key associated with the public key below.

## Public Key
```plaintext
-----BEGIN PUBLIC KEY-----
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA0oqJIrK5a/AXxjE2LWgn
bD8lYlFqOh4Vwd8x8U+qEylBuGHyx5pLPO4DbV5BG/q8KrSy5Qfcl6x8XBRqlb+m
vKKEvGZrkfE5Kdp5tk8oX9Ao13grTT7YWmlhlhAcK5DZW3nRmTHv9N8mFViCTt0V
qpyzLwVjd4Xr6IX8SHofnpG6o1M8Rc8T6O5tCv9xTWR3dFY4XezISy6/ozOrRym8
V9cUq+oD+0GzNdTQ9ElczZuf8xlTDrwBdHJ9TQC8NPHq9B/YF57HdMlMAA3hbOXZ
JWpLMYnvKzLsJkNHeZtG4Ro29yN55E6Y38tM9p8lbD41kcYk6mNTNHk8HYMiUDEu
+wIDAQAB
-----END PUBLIC KEY-----
```
## Signed Message
The following message was signed using the private key:
```plaintext
This is a proof of ownership for my GitHub repository.
```
## Signature
The cryptographic signature for the signed message is stored in `signature.bin`.

## Verification Instructions
To verify the ownership:
1. **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    ```

2. **Run the Python script run.py:**
    ```bash
    python run.py
    ```
3. **`signature.bin`**
This file contains the binary cryptographic signature generated using the private key.

## How to Test this repo?
1. Clone the repository:
    ```bash
    git clone https://github.com/tryevertthhub/repo-template.git
    cd repository-verification
    ```
2. Run the verification script:
    ```bash
    python run.py
    ```
3. Check the output:
- If successful: 🎉 Signature is valid! This repository is owned by the key holder. ✅
- If unsuccessful: ❌ Signature verification failed: [Error details]
