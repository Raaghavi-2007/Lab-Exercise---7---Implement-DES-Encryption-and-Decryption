# Lab-Exercise---7---Implement-DES-Encryption-and-Decryption

# Aim:
To use the Data Encryption Standard (DES) algorithm for a practical application, such as securing sensitive data transmission in financial transactions.

# Procedure:

1. DES is based on a symmetric key encryption technique that encrypts data in 64-bit blocks.
2. DES uses a Feistel network structure with 16 rounds of processing for encryption.
3. DES has a 64-bit key, but only 56 bits are used for encryption (the remaining 8 bits are for parity).
4. DES applies initial and final permutations along with 16 rounds of substitution and permutation transformations to produce ciphertext.

# Program:
```
from Crypto.Cipher import DES
from Crypto.Util.Padding import pad, unpad

key = b'12345678'  
cipher = DES.new(key, DES.MODE_ECB)

text = b"HelloDES!"  

padded_text = pad(text, 8)

encrypted = cipher.encrypt(padded_text)

decrypted_padded = cipher.decrypt(encrypted)
decrypted = unpad(decrypted_padded, 8)

print("Original:", text)
print("Encrypted:", encrypted)
print("Decrypted:", decrypted)
```

# Output:

<img width="1917" height="872" alt="image" src="https://github.com/user-attachments/assets/27e3cb53-65e4-4312-b127-544f91225325" />
<img width="1917" height="801" alt="image" src="https://github.com/user-attachments/assets/078d5dd3-9ed4-4929-a394-d20a1959f769" />

# Result:
The DES Encryption and Decryption program is executed successfully.
