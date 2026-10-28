# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main()
{
    char text[100];
    int shift, i;

    printf("Enter text: ");
    fgets(text, sizeof(text), stdin);

    printf("Enter key: ");
    scanf("%d", &shift);

    shift = ((shift % 26) + 26) % 26;

    for (i = 0; text[i] != '\0'; i++)
    {
        if (text[i] >= 'a' && text[i] <= 'z')
            text[i] = (text[i] - 'a' + shift) % 26 + 'a';

        else if (text[i] >= 'A' && text[i] <= 'Z')
            text[i] = (text[i] - 'A' + shift) % 26 + 'A';
    }

    printf("Encrypted text: %s", text);

    for (i = 0; text[i] != '\0'; i++)
    {
        if (text[i] >= 'a' && text[i] <= 'z')
            text[i] = (text[i] - 'a' - shift + 26) % 26 + 'a';

        else if (text[i] >= 'A' && text[i] <= 'Z')
            text[i] = (text[i] - 'A' - shift + 26) % 26 + 'A';
    }

    printf("Decrypted text: %s", text);

    return 0;
}
```

## OUTPUT:
<img width="1907" height="875" alt="image" src="https://github.com/user-attachments/assets/4028e097-5c76-4eb7-8787-ba54dc7b3ff0" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
