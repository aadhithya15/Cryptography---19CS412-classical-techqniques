# Cryptography---19CS412-classical-techqniques


# Rail Fence Cipher
Rail Fence Cipher using with different key values

# AIM:

To develop a simple C program to implement Rail Fence Cipher.

## DESIGN STEPS:

### Step 1:

Design of Rail Fence Cipher algorithnm 

### Step 2:

Implementation using C or pyhton code

### Step 3:

Testing algorithm with different key values. 

## PROGRAM:
```

#include<stdio.h>
#include<conio.h>
#include<string.h>

int main()
{
    int i, j, k, l;
    char a[20], c[20], d[20];

    printf("\n\t\t RAIL FENCE TECHNIQUE");
    printf("\n\nEnter the input string : ");
    gets(a);
    l = strlen(a);

    for(i = 0, j = 0; i < l; i++)
    {
        if(i % 2 == 0)
            c[j++] = a[i];
    }
    for(i = 0; i < l; i++)
    {
        if(i % 2 == 1)
            c[j++] = a[i];
    }
    c[j] = '\0';

    printf("\nCipher text after applying rail fence :");
    printf("%s", c);

    if(l % 2 == 0)
        k = l / 2;
    else
        k = (l / 2) + 1;

    for(i = 0, j = 0; i < k; i++)
    {
        d[j] = c[i];
        j = j + 2;
    }
    for(i = k, j = 1; i < l; i++)
    {
        d[j] = c[i];
        j = j + 2;
    }
    d[l] = '\0';

    printf("\nText after decryption : ");
    printf("%s", d);

    return 0;
}
```

## OUTPUT:
![image](https://github.com/surrey-78/Cryptography---19CS412-classical-techqniques/assets/119559366/a5f4e5a4-6c59-4a3c-a9b8-f29d790e19fb)



## RESULT:
The program is executed successfully
