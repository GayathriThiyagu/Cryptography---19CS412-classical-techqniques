# 14. HASH ALGORITHM

# AIM:
To generate a simple hash of a given message using a custom hash function,

# ALGORITHM:
Input a message from the user.

Use a basic custom hash function that applies simple operations like XOR and addition on the characters of the message.

Convert the resulting hash into a hexadecimal format.

Display the computed hash to the user.

Optionally verify the hash by recomputing it and comparing it with a received hash.

# PROGRAM:
```
Program developed by: T. Gayathri
Reg. No: 212223100007

#include <stdio.h>
#include <string.h>

// Function to compute a simple hash using XOR and addition
void computeSimpleHash(const char *message, unsigned char *hash) {
    unsigned char temp = 0;
    for (int i = 0; message[i] != '\0'; i++) {
        temp ^= message[i];  // XOR each character
        temp += message[i];  // Add each character's value
    }
    *hash = temp;  // Store the result in the hash
}

int main() {
    char message[256];  // Buffer for the input message
    unsigned char hash; // Buffer for the hash (only 1 byte for simplicity)
    char receivedHash[3]; // Buffer for input of received hash (in hex format)

    // Step 1: Input the message
    printf("Enter the message: ");
    scanf("%s", message);

    // Step 2: Compute the simple hash
    computeSimpleHash(message, &hash);

    // Step 3: Display the computed hash in hexadecimal format
    printf("Computed Hash (in hex): %02x\n", hash);

    // Step 4: Input the received hash
    printf("Enter the received hash (in hex): ");
    scanf("%s", receivedHash);

    // Step 5: Convert received hash from hex string to an unsigned char
    unsigned int receivedHashValue;
    sscanf(receivedHash, "%02x", &receivedHashValue);

    // Step 6: Compare the computed hash with the received hash
    if (hash == receivedHashValue) {
        printf("Hash verification successful. Message is unchanged.\n");
    } else {
        printf("Hash verification failed. Message has been altered.\n");
    }

    return 0;
}
```

# OUTPUT:

![Screenshot 2024-11-11 033119](https://github.com/user-attachments/assets/692163b0-8a0e-4883-885f-8e1716896f3f)

# RESULT: 
The Program is executed successfully..
