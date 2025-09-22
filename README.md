# cyber-security-task_01
def caesar_cipher(text, shift, mode):
    result = ""
    for char in text:
        if char.isalpha():
            ascii_offset = ord('A') if char.isupper() else ord('a')
            result += chr((ord(char) - ascii_offset + shift * mode) % 26 + ascii_offset)
        else:
            result += char
    return result

def main():
    print("Caesar Cipher Program")
    message = input("Enter your message: ")
    shift = int(input("Enter shift value: "))
    
    encrypted = caesar_cipher(message, shift, 1)
    decrypted = caesar_cipher(encrypted, shift, -1)
    
    print(f"Encrypted message: {encrypted}")
    print(f"Decrypted message: {decrypted}")

if _name_ == "_main_":
    main()
