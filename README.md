# Lab-Exercise---1---Caesar-Cipher

## Aim:
To encrypt and decrypt the given message by using Ceaser Cipher encryption algorithm.

## Procedure:

1. Define a function caesar_cipher(text, shift) to perform encryption and decryption.
2. Initialize an empty string result to store the converted message.
3. Iterate through each character in the input text.
4. Check whether the character is uppercase or lowercase and shift it according to the given key using ASCII values and modulo 26.
5. Keep spaces, numbers, and special characters unchanged.
6. Get the user's choice (e for encryption or d for decryption), the message, and the shift value as input.
7. If the choice is e, encrypt the message using the given shift value.
8. If the choice is d, decrypt the message by reversing the shift direction.
9. Display the resulting encrypted or decrypted message. If the choice is invalid, display an error message.

## Program:
```
def caesar_cipher(text, shift):
    result = ""
    for char in text:
        if char.isupper():
            result += chr((ord(char) - ord('A') + shift) % 26 + ord('A'))
        elif char.islower():
            result += chr((ord(char) - ord('a') + shift) % 26 + ord('a'))
        else:
            result += char  # Keep spaces, numbers, and punctuation unchanged
    return result

# Get user choices
choice = input("Encrypt or decrypt? (e/d): ").lower()
message = input("Enter your message: ")
shift = int(input("Enter shift value: ")) % 26

# Handle choice logic correctly
if choice == "d":
    # For decryption, we reverse the shift direction
    shift = -shift
    print("Result:", caesar_cipher(message, shift))

elif choice == "e":
    # For encryption, we use the shift as entered
    print("Result:", caesar_cipher(message, shift))

else:
    # Handle actual invalid choices
    print("Invalid choice.")
```

## Output:

<img width="1562" height="830" alt="image" src="https://github.com/user-attachments/assets/d651b535-767f-4fed-bad4-226e0583b61f" />

## Result:

Thus, the Caesar Cipher algorithm for encryption and decryption was implemented successfully using Python.



         
  
