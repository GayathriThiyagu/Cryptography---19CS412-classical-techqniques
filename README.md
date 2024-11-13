# 10. SIMULATION OF DIFFIE HELLMAN ALGORITHM 

# AIM:
To implement key exchange between users using Diffie Hellman algorithm. 

# ALGORITHM:
1. Get the input for prime number p. 
2. Calculate the primitive root of p that is g. 
3. Calculate private keys for both users using p and g values. 
4. Similarly, secret keys for both users are calculated.

# PROGRAM:
```
Program developed by: T. Gayathri
Reg. No: 212223100007

#include <math.h> 
#include <stdio.h> 
long long int power(long long int a, long long int b, 
long long int P) 
{ 
    if (b == 1) 
    return a; 
    else 
    return (((long long int)pow(a, b)) % P); 
} 
int main() 
{ 
    long long int P, G, x, a, y, b, ka, kb; 
    printf("\n                  *****Diffie-Hellman Key Exchange algorithm*****\n\n"); 
    printf("\n\nEnter the value of P: "); 
    scanf("%lld",&P); // A prime number P is taken 
    printf("The value of P: %lld\n", P); 
printf("Enter the value of G (Primitive root of P): "); 
scanf("%lld",&G); // A primitive root for P, G is taken 
printf("The value of G: %lld\n\n", G); 
a = 4; // a is the chosen private key 
printf("The private key a for Alice : %lld\n", a); 
x = power(G, a, P); // gets the generated key 
// Bob will choose the private key b 
b = 3; // b is the chosen private key 
printf("The private key b for Bob : %lld\n\n", b); 
y = power(G, b, P); // gets the generated key 
ka = power(y, a, P); // Secret key for Alice 
kb = power(x, b, P); // Secret key for Bob 
printf("Secret key for the Alice is : %lld\n", ka); 
printf("Secret Key for the Bob is : %lld\n", kb); 
return 0; 
} 
```
# OUTPUT:

![image](https://github.com/user-attachments/assets/6f2ad3a4-3354-4940-93e1-ecba1a6fa69a)

# RESULT:
Hence, the simulation of Diffie Hellman algorithm is successfully done. 
