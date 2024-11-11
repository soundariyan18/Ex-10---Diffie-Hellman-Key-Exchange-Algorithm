# Ex-10---Diffie-Hellman-Key-Exchange-Algorithm
```
Name: Soundariyan MN
212222230146
```
<h1>AIM: </h1>

To implement key exchange between users using Diffie Hellman algorithm.

<h2>ALGORITHM:</h2> 

step 1.Get the input for prime number p 
step 2.Calculate the primitive root of p that is g. 
step 3.Calculate private keys for both users using p and g values. 
step 4.Similarly, secret keys for both users are calculated. 

<h1>PROGRAM:</h1>

```c
#include <math.h>
#include <stdio.h>

long long int power(long long int a, long long int b, long long int P) {
    if (b == 1) 
        return a;
    else 
        return ((long long int)pow(a, b)) % P;
}

int main() {
    long long int P, G, x, a, y, b, ka, kb;
    
    printf("\n***** Diffie-Hellman Key Exchange Algorithm *****\n");
    
    // Input for P
    printf("\nEnter the value of P: ");
    scanf("%lld", &P);
    printf("The value of P: %lld\n", P);
    
    // Input for G
    printf("Enter the value of G (Primitive root of P): ");
    scanf("%lld", &G);
    printf("The value of G: %lld\n\n", G);
    
    // Private key for Alice
    a = 4;
    printf("The private key a for Alice: %lld\n", a);
    x = power(G, a, P);
    
    // Private key for Bob
    b = 3;
    printf("The private key b for Bob: %lld\n\n", b);
    y = power(G, b, P);
    
    // Secret keys
    ka = power(y, a, P);
    kb = power(x, b, P);
    
    printf("Secret key for Alice is: %lld\n", ka);
    printf("Secret key for Bob is: %lld\n", kb);
    
    return 0;
}
```

<h2>Output:</h2>

![image](https://github.com/user-attachments/assets/29483223-1bde-4659-b22d-4fc21a70ec2d)

<h2>Result</h2>

Hence, the simulation of Diffie Hellman algorithm is successfully done.

