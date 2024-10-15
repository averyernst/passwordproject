def password_check():
    password=(input("please imput a password"))
    if len((password))>=8:
        print("length: ✔")
    else: 
        print("length: X")
    numbers=["1","2","3","4","5","6","7","8","9","0"]
    
    
    for item in numbers:
        if item in password:
            has_number=True
        if item not in password: 
            has_number=False
    if has_number==True:
        print("number ✔")
    if has_number==False:
        print("number: X")


