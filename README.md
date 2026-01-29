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
def caesar_encrypt(text, shift):
    result = ""

    for char in text:
        if char.isalpha():   # check if letter
            start = ord('A') if char.isupper() else ord('a')
            result += chr((ord(char) - start + shift) % 26 + start)
        else:
            result += char   # keep spaces/symbols same

    return result


def caesar_decrypt(text, shift):
    return caesar_encrypt(text, -shift)


# Main program
message = input("Enter message: ")
key = int(input("Enter shift value: "))

encrypted = caesar_encrypt(message, key)
print("Encrypted Text:", encrypted)

decrypted = caesar_decrypt(encrypted, key)
print("Decrypted Text:", decrypted)
```

## OUTPUT:

<img width="459" height="228" alt="image" src="https://github.com/user-attachments/assets/cf450ed9-f907-428a-afb1-81515729fbb6" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
