# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
```
STEP 1:
AES is based on a design principle known as a substitution–permutation.
STEP 2:
AES does not use a Feistel network like DES, it uses variant of Rijndael.
STEP 3:
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
STEP 4:
AES operates on a 4 × 4 column-major order array of bytes, termed the state
```
# PROGRAM:
```
NAME : LOGA MITHRA R
REGISTER NUMBER : 212223100027

#include <stdio.h>
#include <string.h>

void xor_encrypt_decrypt(char *input, char *key) {
    int input_len = strlen(input);
    int key_len = strlen(key);
    for (int i = 0; i < input_len; i++) {
        input[i] = input[i] ^ key[i % key_len];
    }
}

int main() {
    char url[] = "WELCOME";
    char key[] = "secretkey";
    
    printf("Original text: %s\n", url);
    xor_encrypt_decrypt(url, key);
    printf("Encrypted text: %s\n", url);
    xor_encrypt_decrypt(url, key);
    printf("Decrypted text: %s\n", url);

    return 0;
}
```
# OUTPUT:

![image](https://github.com/user-attachments/assets/d5aa07c8-e09a-4313-a581-a6931e085329)

# RESULT:
The program has been run successfully
