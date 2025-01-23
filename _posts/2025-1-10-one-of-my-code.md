---
title : a code of mine
date : 2025-1-10 00:00:00 +0800
categories : [python]
tags : [one of my code]
image :
    path : assets\images\teacher2.jpg
---

this is a code where you can inssert how many number of people y want to buy of the last remaining 10 tickets.
hope y enjoy

```python
tiket=10
start=0
stop=int(input("masukkan berapa orang ingin membeli tiket: "))
orang=[]

while start<stop:
    while tiket>0:
        start+=1
        nama=input(f"masukkan nama pengunjung {start} : ")
        beli=int(input("masukkan jumlah tiket yang ingin dibeli: "))
        orang.append(nama)
        if tiket<beli:
            print(f"maaf tiket tidak cukup.Tiket sisa {tiket}")
            break
        if tiket>=beli:
            tiket= tiket - beli
            print(f"{nama} berhasil membeli {beli} tiket. tiket sisa : {tiket}")
            break
        orang.pop(0)
    if tiket<=0:
        print("tiket habis")
        break
```