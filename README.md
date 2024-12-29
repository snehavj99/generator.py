# generator.py
#Project Title: Password Generator,Python-based application designed to generate strong,and randomized passwords to provide a secure and efficient way to create passwords that meet specific length and complexity
import random     #built in function to generate a random number
import string     #built in function to generate string module

def generate_password(length):     #the define's a function that generates the password
    characters = string.ascii_letters + string.digits + string.punctuation    #string concatenation of letters,digits,symbols.
    return ''.join(random.choice(characters) for _ in range(length))          #selects a random characters from string and returns

def main():
    length = int(input("Enter the desired password length please (min. 4): "))  
    print("Generated Password : ", generate_password(length))

if __name__ == "__main__":
    main()

