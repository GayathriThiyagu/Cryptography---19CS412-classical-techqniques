# 2. PLAYFAIR CIPHER

# AIM:
 To implement Playfair Cipher using C program

# ALGORITHM:
1. Input the plaintext and the key
 2. Create the 5x5 cipher matrix
 3. Prepare the plaintext
 4. Encrypt the plaintext digraphs
 5. Output the ciphertext

# PROGRAM:
```
Program developed by: T. Gayathri
Reg. No: 212223100007

 #include<stdio.h> 
#include<string.h> 
int main() 
{ 
unsigned int a[3][3]={{6,24,1},{13,16,10},{20,17,15}}; 
unsigned int b[3][3]={{8,5,10},{21,8,21},{21,12,8}}; 
int i,j, t=0; 

    unsigned int c[20],d[20]; 
    char msg[20]; 
    printf("Enter plain text: "); 
    scanf("%s",msg); 
    for(i=0;i<strlen(msg);i++) 
    { 
        c[i]=msg[i]-65; 
        printf("%d ",c[i]); 
    } 
    for(i=0;i<3;i++) 
    { 
        t=0; 
        for(j=0;j<3;j++) 
        { 
            t=t+(a[i][j]*c[j]); 
        } 
        d[i]=t%26; 
    } 
    printf("\nEncrypted Cipher Text :"); 
    for(i=0;i<3;i++) 
    printf(" %c",d[i]+65); 
    for(i=0;i<3;i++) 
    { 
        t=0; 
        for(j=0;j<3;j++) 
        { 
            t=t+(b[i][j]*d[j]); 
        } 
        c[i]=t%26; 
    } 
    printf("\nDecrypted Cipher Text :"); 
    for(i=0;i<3;i++) 
    printf(" %c",c[i]+65); 
    return 0; 
}
```
# OUTPUT:

![Screenshot 2024-11-13 040612](https://github.com/user-attachments/assets/c24393ab-6d83-49c6-8216-8b0b2177fd92)

# RESULT:
Thus the implementation of Playfair Cipher using C program is executed and verified.
