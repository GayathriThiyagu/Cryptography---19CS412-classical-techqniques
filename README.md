# 5. RAIL FENCE CIPHER 

# AIM:
To implement Rail fence cipher using C programming 

# ALGORITHM:
1: Choose the Number of Rails 
2: Write the Plaintext in a Zigzag Pattern 
3: Read Each Rail Row-by-Row 
 4: Combine the Letters from All Rails 
 5: Output the Ciphertext

# PROGRAM:
```
Program: developed by: T. Gayathri
Reg. No: 212223100007

#include <stdio.h> 
#include<string.h> 
void main() 
{ 
    int i,j,k,l; 
    char a[20],c[20],d[20]; 
    printf("\n\t\t RAIL FENCE TECHNIQUE"); 
    printf("\n\nEnter the input string : "); 
    gets(a); 
    l=strlen(a); 
    for(i=0,j=0;i<l;i++) 
    { 
         
        if(i%2==0) 
        c[j++]=a[i]; 
    } 
    for(i=0;i<l;i++) 
    { 
         if(i%2==1) 
         c[j++]=a[i]; 
 
    } 
    c[j]='\0'; 
    printf("\nCipher text after applying rail fence :"); 
    printf("\n%s",c); 
    if(l%2==0) 
     k=l/2; 
    else 
     k=(l/2)+1; 
    for(i=0,j=0;i<k;i++) 
    { 
        d[j]=c[i]; 
        j=j+2; 
 
    } 
    for(i=k,j=1;i<l;i++) 
    { 
        d[j]=c[i]; 
        j=j+2; 
         
    } 
    d[l]='\0'; 
    printf("\nText after decryption : "); 
    printf("%s",d); 
    
} 
```
# OUTPUT:

![image](https://github.com/user-attachments/assets/d84257d1-bcd8-41e4-b6b2-a01b6e395c2f)

# RESULT:
Thus the implementation of Rail Fence cipher using C programming was executed and verified.  
