# generator.py

import random    

import string     

def generate_password(length):    
    characters = string.ascii_letters + string.digits + string.punctuation                                                        
    return ''.join(random.choice(characters) for _ in range(length))                                                            

def main():
    length = int(input("Enter the desired password length please (min. 4): "))  
    print("Generated Password : ", generate_password(length))

if __name__ == "__main__":
    main()

