# harf_ve_sayi_adedi_bulma
Argüman olarak bir string alan, bu string içindeki harf ve rakam sayısını bulan Python programını yazalım.
Bu programda;
Sadece harf ve rakamların sayısı dikkate alınacak,
Fonksiyon argüman olarak string alacak,  
Hesaplama işlemi bu fonksiyon içerisinde yaptırılacak,
Fonksiyon sözlük döndürecek ve 
Rakam veya string olup olmadığını kontrol eden fonksiyon kullanılacaktır.
```python
def harf_ve_sayi_adedi_bulma(karakterler:str) -> dict:
    
    dict_={"NUMBERS":0,"LETTERS":0}     
    
    for karakter in karakterler:
        if karakter.isnumeric():
            dict_["NUMBERS"]+=1
        elif karakter.isalpha():
            dict_["LETTERS"]+=1
        else:
           continue
    return dict_        

sözlük= str(input("Bir değer giriniz: "))
karakterler=harf_ve_sayi_adedi_bulma(sözlük)
print(karakterler)
```
Eğer bu programı sözlük içine atmasaydık şu şekilde de tanımlayabilirdik:
```python
def harf_ve_sayi_adedi_bulma(karakterler):
    
    num=0
    ch=0
    
    for karakter in karakterler:
        if karakter.isnumeric():
            num+=1
        elif karakter.isalpha():
            ch+=1
        else:
           continue
    
    return((f"'LETTER': {ch}, 'NUMBER': {num}"))    

sözlük= str(input("Bir değer giriniz: "))
karakterler=harf_ve_sayi_adedi_bulma(sözlük)
print(karakterler) 
```
