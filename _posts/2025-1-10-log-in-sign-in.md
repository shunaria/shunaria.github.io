---
title : a log in and sign in code
date : 2025-1-10 00:00:00 +0800
categories : [a code of mine]
tags : [just a simple code]
---
another code that i try to make to be use for log in and sign in
as the title suggest its just a simple code so that can be use for log in and sign in 
hopefully you guys can find some use for this simpel code

```python
user=["shun","tooya"]
pas=["aria","911"]

while True:

    
    print("silahkan pilih opsi yang anda inginkan")
    print("1.sign in")
    print("2.log in")
    pilihan = str(input("silahkan pilih anda ingin opsi ke berapa menggunakan angka:"))

    if pilihan =="1":
        username = str(input("masukkan usename yang ingin anda gunakan:"))
        password = str(input("silahkan masukkan password yang ingin anda gunakan:"))
        for i in range (len(user)):
            if username == user[i]:
                print("username sudah ada")
            else:
                user.append(username)
                pas.append(password)
        

    if pilihan =="2":
        loggedin = "false"
        user_anda = str(input("masukkan username anda:"))
        pass_anda = str(input("masukkan password anda:"))
        if user_anda in user :
            index = user.index(user_anda)
            if pass_anda == pas[index]:
                loggedin="True"
        if loggedin=="True":
            print("anda telah masuk")
            break
        if loggedin=="false":
            print("salah")
```