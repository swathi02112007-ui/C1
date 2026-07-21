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
~~~
#include <stdio.h>
#include <string.h>

int main()
{
    char text[100];
    int key, i;

    printf("Enter the plain text: ");
    scanf("%s", text);

    printf("Enter the key value: ");
    scanf("%d", &key);

    for(i = 0; text[i] != '\0'; i++)
    {
        if(text[i] >= 'A' && text[i] <= 'Z')
        {
            text[i] = ((text[i] - 'A' + key) % 26 + 26) % 26 + 'A';
        }
        else if(text[i] >= 'a' && text[i] <= 'z')
        {
            text[i] = ((text[i] - 'a' + key) % 26 + 26) % 26 + 'a';
        }
    }

    printf("Cipher Text: %s\n", text);

    return 0;
}
~~~

## OUTPUT:

![alt text](<Screenshot 2026-07-21 142734.png>)

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
