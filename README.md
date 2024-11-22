import random

def password_check():
    strength_score=0
    password=(input("please imput a password"))
    if len((password))>=8:
        print("length: ✔")
        strength_score+=1
    else: 
        print("length: X")
    
    has_number = False
    for char in password:
        if char.isdigit():  
            has_number = True
    if has_number:
        print("number: ✔")
        strength_score+=1
    else:
        print("number: X")
        
    symbols = "!@#$,%&*+-./:;()<=>?^_'|"
    has_symbol=False
    for char in symbols:
        if char in password:
            has_symbol = True 
    if has_symbol:
        print("symbol: ✔")
        strength_score+=1
    else:
        print("symbol: X")

    has_uppercase=False
    for char in password: 
        if char.isupper():
            has_uppercase=True
    if has_uppercase:
        print("Uppercase letter: ✔")
        strength_score+=1
    else:
        print("Uppercase letter: X")
    
    if len(password)>8 and has_number==True and has_symbol==True and has_uppercase==True:
        print("Password is sufficiently strong")
    else:
        print("Password is not strong enough. Another password is reccmoended")
    if strength_score == 4:
        print("Password strength: strong")
    elif strength_score == 3:
        print("Password strength: fair")
    else:
        print("Password strength: Weak")
        password = password_fix(password)
    return password


def password_fix(password):
    
    has_number = False
    for char in password:
        if char.isdigit():
            has_number = True
    if not has_number:
        password += random.choice("0123456789")
        print("Added a number to the password.")
    
    has_uppercase = False
    for char in password:
        if char.isupper():
            has_uppercase = True
    if not has_uppercase:
        password += random.choice("ABCDEFGHIJKLMNOPQRSTUVWXYZ")
        print("Added an uppercase letter to the password.")
    
    symbols = "!@#$,%&*+-./:;()<=>?^_'|"
    has_symbol = False
    for char in password:
        if char in symbols:
            has_symbol = True
    if not has_symbol:
        password += random.choice(symbols)
        print("Added a special character to the password.")

    while len(password) < 8:
        password += random.choice("ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789")
    print("Password is too short. Added characters to meet the minimum length requirement.")
    print("Suggestions for a new password:\n")
    print("New password:", password)

    return password

