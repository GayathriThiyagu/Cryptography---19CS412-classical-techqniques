# ELGAMAL ALGORITHM 

# AIM:
To encrypt and decrypt a message using Elgamal Algorithm 

# ALGORITHM:
 Choose a large prime number p and a generator g of the multiplicative group of integers
 modulo p. Alice chooses a private key and computes her public key as public_key =
 g^private_key mod p. To encrypt a message, Bob chooses a random number k and
 computes a ciphertext pair (c1, c2). To decrypt the message, Alice uses her private key and
 computes the original message. The decrypted message is verified to be the same as the
 orginal.

# PROGRAM:
```
Program Developed by: T. Gayathri
Reg. No: 212223100007

 #include <stdio.h>
 // Function to perform modular exponentiation
 long long int modExp(long long int base, long long int exp, long long int mod) {
 long long int result = 1;
 while (exp > 0) {
 if (exp % 2 == 1) {
 result = (result * base) % mod;
 }
 base = (base * base) % mod;
 exp /= 2;
 }
 return result;
 }
 int main() {
 long long int p, g, privateKeyA, publickeyA;
 long long int k, message, c1, c2, decryptedMessage;
 // Input for prime number p and generator g
 printf("Enter a large prime number (p): ");
 scanf("%lld", &p);
 printf("Enter a generator (g): ");
 scanf("%lld", &g);
 // Alice's private key input
 printf("Enter Alice's private key: ");
 scanf("%lld", &privateKeyA);
 // Calculate Alice's public key
publickeyA = modExp(g, privateKeyA, p);
 printf("Alice's public key: %lld\n", publickeyA);
 // Step 4: Bob inputs the message to be encrypted and selects a random k
 printf("Enter the message to encrypt (as a number): ");
 scanf("%lld", &message);
 printf("Enter a random number k: ");
 scanf("%lld", &k);
 // Encryption process
 c1 = modExp(g, k, p);
 c2 = (message * modExp(publickeyA, k, p)) % p;
 printf("Encrypted message (c1, c2): (%lld, %lld)\n", c1, c2);
 return 0;
 }

```
# OUTPUT:

![WhatsApp Image 2024-11-11 at 02 54 20_ea3662b4](https://github.com/user-attachments/assets/d53bdfd3-230a-486c-b3de-74502ceb2c21)


# RESULT:
Thus the encryption and decryption of message using Engamal Algorithm is executed and verified successfully
