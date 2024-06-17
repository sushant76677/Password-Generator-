#Password_Generator
import random
import string

def generate_password(length):
    characters = string.ascii_letters + string.digits + string.punctuation
    
    
    password = ''.join(random.choice(characters) for i in range(length))
    
    return password

 
try:
    password_length = int(input("Enter the desired length of your password: "))
    
    if password_length <= 0:
        print("Password length must be greater than zero.")
    else:
        
        password = generate_password(password_length)
        print("Generated password:", password)

except ValueError:
    print("Invalid input. Please enter a valid integer.")
