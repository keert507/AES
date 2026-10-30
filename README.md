# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```
#include <stdio.h> 
#include <string.h> 

void xorCrypt(char *in, char *key) { 
    for (int i = 0; in[i]; i++) {
        in[i] ^= key[i % strlen(key)]; 
    }
} 

int main() { 
    char msg[256], key[64]; 

    printf("Enter Text: ");
    fgets(msg, sizeof(msg), stdin);
    msg[strcspn(msg, "\n")] = 0;

    printf("Enter Key: ");
    fgets(key, sizeof(key), stdin);
    key[strcspn(key, "\n")] = 0;

    printf("\nOriginal: %s\n", msg); 
    
    xorCrypt(msg, key); 
    printf("Encrypted: %s\n", msg); 
    
    xorCrypt(msg, key); 
    printf("Decrypted: %s\n", msg); 
    
    return 0; 
}
```

# OUTPUT:

<img width="438" height="397" alt="image" src="https://github.com/user-attachments/assets/27a63ba8-5b76-4923-a46d-c5512385e4f9" />


# RESULT:



