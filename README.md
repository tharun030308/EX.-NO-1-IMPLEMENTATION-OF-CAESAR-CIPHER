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
int main() { 
char text[100], original[100]; 
int key, i; 
printf("Enter the plain text: "); 
fgets(text, sizeof(text), stdin); 
text[strcspn(text, "\n")] = '\0'; 
 
    printf("Enter the key value: "); 
    scanf("%d", &key); 
 
    key = ((key % 26) + 26) % 26; 
 
    strcpy(original, text); 
 
    for (i = 0; text[i] != '\0'; i++) { 
        if (text[i] >= 'A' && text[i] <= 'Z') 
            text[i] = (text[i] - 'A' + key) % 26 + 'A'; 
        else if (text[i] >= 'a' && text[i] <= 'z') 
            text[i] = (text[i] - 'a' + key) % 26 + 'a'; 
    } 
 
    printf("Encrypted text: %s\n", text); 
 
    for (i = 0; text[i] != '\0'; i++) { 
        if (text[i] >= 'A' && text[i] <= 'Z') 
            text[i] = (text[i] - 'A' - key + 26) % 26 + 'A'; 
        else if (text[i] >= 'a' && text[i] <= 'z') 
            text[i] = (text[i] - 'a' - key + 26) % 26 + 'a'; 
    } 
 
    printf("Decrypted text: %s\n", text); 
 
    return 0; 
}
```
## OUTPUT:
<img width="295" height="82" alt="image" src="https://github.com/user-attachments/assets/a4289528-59ba-449b-9668-ad0ecfee9a09" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
