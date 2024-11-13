# 6.  PSEUDORANDOM NUMBER GENERATION  

# AIM: 
  To develop a C program to implement Pseudorandom Number Generation using 
Standard Libraries

# ALGORITHM:
1. Including all necessary Header files. 
2. Input the number of random numbers and range. 
3. Seed the random number generator. 
4. Initialize a loop. 
5. Generate the Random Numbers. 
6. Print the random numbers. 

# PROGRAM:
```
Program developed by: T. Gayathri
Reg. No: 212223100007

#include <stdio.h> 
#include <stdlib.h> 
#include <time.h> 
 
int main()  
{ 
    int count, min, max; 
    printf("Enter the number of random numbers to generate: "); 
    scanf("%d", &count); 
    printf("Enter the minimum value: "); 
     
    scanf("%d", &min); 
    printf("Enter the maximum value: "); 
    scanf("%d", &max); 
    srand(time(NULL)); 
    printf("Pseudorandom numbers:\n");    
    for (int i = 0; i < count; i++)  
    { 
        int random_number = (rand() % (max - min + 1)) + min; 
        printf("%d\n", random_number); 
    } 
    return 0; 
} 
```
# OUTPUT:

![image](https://github.com/user-attachments/assets/521dc50c-c98d-4dc4-961f-945af5c9d5ec)

# RESULT: 
 Thus the implementation of Pseudorandom Number using C program is executed 
and verified successfully. 
