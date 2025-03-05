# h7 Maalisuora

Tekijä: Marianne Taipale   
Kotitehtävä kurssille: Linux Palvelimet ICI003AS2A-3008  
Tehtävänanto: https://terokarvinen.com/linux-palvelimet/   

## Laitteeni
- Lenovo Yoga Pro 7
- Ryzen 7 Prosessori

## a) Hei maailma
#### 5.3.2025 Klo. 12:58

Tehtävän tarkoituksena on ajaa "Hei maailma" kolmella eri ohjelmointikielellä. Valitsin kieliksi, javan, pythonin ja C:n. 

Ensimmäiseksi päivitin, ennenkuin aloin lataamaan Javaa, ja C:tä 

![image](https://github.com/user-attachments/assets/3271765a-dd01-4a4f-b03b-932f505b0c95)

### Java 

Aloitin asentamalla Java paketin komennolla:

- $ sudo apt install default-jdk

![image](https://github.com/user-attachments/assets/57fba0d1-c37f-4358-a888-410e12568b69)

Asennetun java version näin komennolla: 

- $ java --version

![image](https://github.com/user-attachments/assets/8b04319d-c80a-4275-8554-fbf20798325c)

Tein javakansion ja kansiossa avasin micron, että saan lisättyä sinne "Hello World" koodin. 

![image](https://github.com/user-attachments/assets/6cb56ea3-bde4-48a4-8bf3-19f4dd6d8895)

Ilmeisesti lähdekoodi on muutettava konekieliseksi ohjelmaksi, ennekuin ohjelma voidaan ajaa onnistuneesti. 

- $ javac Hello.java

Viimeisenä, katsotaan tulostuuko Hello World teksti nyt oikein.

- $ java Hello

![image](https://github.com/user-attachments/assets/c8122eee-dd67-4017-9ac0-2b350afe2c79)

Lähde: https://wiki.debian.org/Java  
https://docs.oracle.com/javase/8/docs/technotes/tools/windows/javac.html 

### C 

C kielen asennus: 

- $ sudo apt install gcc

Tarkistin, että lataus onnistui samalla tavalla kuin javassa. 

- $ gcc --version

![image](https://github.com/user-attachments/assets/724755a1-3e60-431d-a9f6-fd4a3f44e04d)

Tein ckansion, avasin kansiossa micron.

![image](https://github.com/user-attachments/assets/96d48d32-b9b7-470b-93ea-1dc94f570363)

Lisäsin sinne koodin: 

![image](https://github.com/user-attachments/assets/50057d08-934b-4671-8cb0-ca84f34632b6)

Lopetuksi vielä kokeillaan tulostuuko oikein. 

![image](https://github.com/user-attachments/assets/6fc9c59a-3152-4b15-98b1-2e411b888d22)

Lähde: https://data-flair.training/blogs/install-c-on-linux/

### Python

Muistin, että Python pitäisi olla valmiiksi asennettuna debian ympäristössä, joten tarkistin että se on varmasti asennettu. 

![image](https://github.com/user-attachments/assets/43e3c429-a4ad-4e0a-ab0d-f2d10ccbfd7c)

Sama tapa, kuin edellisissä. Uusi kansio ja microon koodi: 

![image](https://github.com/user-attachments/assets/37865a63-c87a-4aca-a8f8-2f57447020cd)

Suoritetaan komennolla: 

- $ python3 Hello.py

![image](https://github.com/user-attachments/assets/122632fb-b5aa-4576-8787-0ce20a0d7783)

#### Lopetus 5.3.2025 klo. 14:22

## c) Uusi komento

## d) Laboratorioharjoitus

## e) Tyhjä virtuaalikone

## Lähteet
Tero Karvinen, 27.9.2018. Hello World Python3, Bash, C, C++, Go, Lua, Ruby, Java – Programming Languages on Ubuntu 18.04. https://terokarvinen.com/2018/hello-python3-bash-c-c-go-lua-ruby-java-programming-languages-on-ubuntu-18-04/   
Debian Wiki. Java. https://wiki.debian.org/Java  
Oracle. Javac. https://docs.oracle.com/javase/8/docs/technotes/tools/windows/javac.html
