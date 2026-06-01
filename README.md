# Python-simple-encryption-and-decryption  Author: Salem Solomon
Python encryption/decryption program using character shifting.

print('start of A3 program')
# The while loop prompts the user to keep entering a message until they hit enter
while True:
    plaintext = input('Input plaintext message or hit enter to quit: ')
    if not plaintext:
        break
    integer = int(input('enter offset integer value: '))
# by setting encrypt and decrypt to zero, it will enable the program to add to the strings based on the users input
    encrypt = ""
    decrypt = ""
# This code converts the users plaintext into a number, adds the integer value entered, and converts it into a character
# The converted character is then added to the empty string encrypt
    for s in plaintext:
        encrypt += chr(ord(s) + integer)
    print(encrypt)
# This for loop converts encrypted text back into its original form and prints it
    for a in encrypt:
        decrypt += chr(ord(a) - integer)
    print(decrypt)
input('\n\nHit Enter to end program')
