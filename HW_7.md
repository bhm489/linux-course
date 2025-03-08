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

Ensimmäiseksi päivitin ennen kuin aloin lataamaan Javaa, ja C:tä 

![image](https://github.com/user-attachments/assets/3271765a-dd01-4a4f-b03b-932f505b0c95)

### Java 

Aloitin asentamalla Java paketin komennolla:

- $ sudo apt install default-jdk

![image](https://github.com/user-attachments/assets/57fba0d1-c37f-4358-a888-410e12568b69)

Asennetun java version näki komennolla: 

- $ java --version

![image](https://github.com/user-attachments/assets/8b04319d-c80a-4275-8554-fbf20798325c)

Tein java-kansion ja avasin micron:

- $ mkdir javakansio
- $ micro Hello.java

Microon lisäsin yksinkertaisen "Hello, World" java koodin. 

![image](https://github.com/user-attachments/assets/6cb56ea3-bde4-48a4-8bf3-19f4dd6d8895)

Ilmeisesti lähdekoodi on muutettava konekieliseksi ohjelmaksi, ennen kuin ohjelma voidaan ajaa onnistuneesti. 

- $ javac Hello.java

Teksti tulostui nyt oikein:

- $ java Hello

![image](https://github.com/user-attachments/assets/c8122eee-dd67-4017-9ac0-2b350afe2c79)

Lähde: https://wiki.debian.org/Java  
https://docs.oracle.com/javase/8/docs/technotes/tools/windows/javac.html 

### C 

C kielen asennus: 

- $ sudo apt install gcc

Tarkistin, että lataus onnistui samalla tavalla kuin Javan kanssa. 

- $ gcc --version

![image](https://github.com/user-attachments/assets/724755a1-3e60-431d-a9f6-fd4a3f44e04d)

Tein c-kansion, avasin kansiossa micron.

![image](https://github.com/user-attachments/assets/96d48d32-b9b7-470b-93ea-1dc94f570363)

Lisäsin sinne koodin: 

![image](https://github.com/user-attachments/assets/50057d08-934b-4671-8cb0-ca84f34632b6)

Lopetuksi vielä kokeilin tulostuuko teksti oikein. 

![image](https://github.com/user-attachments/assets/6fc9c59a-3152-4b15-98b1-2e411b888d22)

Lähde: https://data-flair.training/blogs/install-c-on-linux/

### Python

Muistin, että Python pitäisi olla valmiiksi asennettuna debian ympäristössä, joten tarkistin että se on varmasti asennettu. 

![image](https://github.com/user-attachments/assets/43e3c429-a4ad-4e0a-ab0d-f2d10ccbfd7c)

Samalla tavalla, kuin edellisissä. Uusi kansio ja microon koodi: 

![image](https://github.com/user-attachments/assets/37865a63-c87a-4aca-a8f8-2f57447020cd)

Suoritetaan komennolla: 

- $ python3 Hello.py

![image](https://github.com/user-attachments/assets/122632fb-b5aa-4576-8787-0ce20a0d7783)

#### Lopetus 5.3.2025 klo. 14:22

## c) Uusi komento
#### 8.3.2025 klo. 10:00 

### Komento, jota kaikki käyttäjät voivat käyttää. 

Ensimmäiseksi tein uuden komennon. Päätin tehdä tämän käyttäen pythonia, ja tein vain yksinkertaisen kertolaskun 10*10.  

Avasin micron ja laitoin sinne seuraavat: 

Yksinkertaisen python koodin.  

![image](https://github.com/user-attachments/assets/a3b8cf27-a41f-4875-9801-4a21eb47bda4)

Lisäsin microon vielä ```#!/usr/bin/python#```, tämä kertoo ohjelmalle, että millä ohjelmalla skripti pitää ajaa, eli minulla pythonilla.

![image](https://github.com/user-attachments/assets/becced62-eaa5-48a7-a728-ac8be8479553)

![image](https://github.com/user-attachments/assets/f9a6ca77-f1db-4dc6-8d3d-50efbaddfef7)

### Oikeudet komennolle: 

Ensiksi tarkastelin, että mitkä oikeudet komennolla oli. 

- $ ls -l tentimes.py

Lisäsin suoritus oikeudet kaikille ryhmille.

 - $ chmod ugo+x tentimes.py 
  
![image](https://github.com/user-attachments/assets/ee8c7fca-ff91-431a-8e21-10055f03f43e)

Komennon oikeudet:

![image](https://github.com/user-attachments/assets/2343bd8f-f576-449e-abd7-322f7c9eb14d)

Kokeilin, että toimiiko python ohjelma ja vaihdoin nimen vielä. 

![image](https://github.com/user-attachments/assets/b9b87d97-2a18-4c6c-b7d7-bc4ebd6e386a)

Seuraavaksi, että ohjelma olisi mahdollista ajaa kaikilla käyttäjillä suoritin komennon: 

- $ sudo cp tentimes /usr/local/bin/

Kokeilin toimiiko ohjelma. Ohjelma nyt toimi eri hakemistoissa ja nyt kaikki käyttäjät pystyivät sen ajaa. 

![image](https://github.com/user-attachments/assets/5e9a6ec0-f03c-4d1e-b889-92b75ae107f9)

#### Lopetus 8.3.2025 klo. 10:55

## d) Laboratorioharjoitus
#### 8.3.2025 klo. 12:17 

Seuraavaksi tehtävänä oli ratkaista jokin vanha laboratorioharjoitus soveltuvin osin. 
Valitsin seuraavan laboratorioharjoituksen ratkaistavaksi: https://terokarvinen.com/2024/arvioitava-laboratorioharjoitus-2024-linux-palvelimet/ 

### Howdy 
```
(Soveltaen)
- Tee kaikkien käyttäjien käyttöön komento 'howdy'
 - Tulosta haluamaasi ajankohtaista tietoa, esim päivämäärä, koneen osoite tms
 - Pelkkä "hei maailma" ei riitä
- Komennon tulee toimia kaikilla käyttäjillä työhakemistosta riippumatta.
```

Tein uuden tiedoston nanolla, johon lisäsin:

- $ sudo nano /usr/local/bin/howdy
  
![image](https://github.com/user-attachments/assets/39cb11cf-7eb6-4bf8-b9ba-67afa98fce25)

Muokkasin oikeuksia, että komento toimisi kaikilla käyttäjillä:

- $ sudo chmod +x /usr/local/bin/howdy

Sitten kokeilin tulostaako "howdy" oikein hakemistosta riippumatta, kyllä tulosti. 

![image](https://github.com/user-attachments/assets/1facbd73-a8c2-4c0a-9839-fd7900c3d711)

### Etusivu uusiksi
```
(Soveltaen)
- Tee yrityksellemme "AI Kakone" kotisivu
- Kotisivu tulee näkyä koneesi IP-osoitteella suoraan etusivulla
- Sivua pitää päästä muokkaamaan normaalin käyttäjän oikeuksin (ilman sudoa).
```

Loin uuden hakemiston, johon tallensin sivun tiedostot. 

![image](https://github.com/user-attachments/assets/ec3b1b29-0f7d-4519-a324-ae3d543aa16c)

Menin hakemistoon ja tein sinne html koodin. 

![image](https://github.com/user-attachments/assets/2f617156-e2a1-45b5-89cb-834e42d3b500)

Loin VirtualHostin ja uuden tiedoston: 

![image](https://github.com/user-attachments/assets/21440c4c-36c1-42d8-8885-6217985f0bb7)

Otin juuri tehdyt asetukset käyttöön komennoilla: 

![image](https://github.com/user-attachments/assets/ca5c910e-649c-40b4-b5f2-29cfb5669fc9)

IP osoitteen sain selville komennolla: 

- $ hostname -I

Menin katsomaan netissä, että toimiiko verkkosivu kun syötän oman IP osoitteeni, ja sillä se näkyi. 

![image](https://github.com/user-attachments/assets/f8b75a5f-c067-45a0-98db-cbd1a1216b84)

### Salattua hallintaa
```
(Soveltaen)
SSH
Tee uusi käyttäjä omalla nimelläsi, esim. minä tekisin "Tero Karvinen test", login name: "terote01"
Automatisoi ssh-kirjautuminen julkisen avaimen menetelmällä, niin että et tarvitse salasanoja, kun kirjaudut sisään. Voit käyttää kirjautumiseen localhost-osoitetta.
```
Tarkastin ensiksi, että ssh on päällä ja toimii: 

![image](https://github.com/user-attachments/assets/ea788434-e3b6-4a45-9196-f06d965c689a)

Tein uuden käyttäjän ja kirjauduin sillä sisään. 

![image](https://github.com/user-attachments/assets/5a935328-22a4-4840-bcd7-9fd341fb0cae)

Loin uudet ssh avaimet: 

-$ ssh-keygen 

Nyt minulla oli ssh avain ja uusi käyttäjä, mutta en osannut tehdä kirjautumista siten, että se ei kysy salasanaa. En ollut varma, miten alottaa tämä.
Yritin katsoa netistä apua, mutta en löytänyt mitään mitä ymmärtäisin. 

#### Lopetus 8.3.2025 klo. 14:45

## Lähteet
Tero Karvinen, 27.9.2018. Hello World Python3, Bash, C, C++, Go, Lua, Ruby, Java – Programming Languages on Ubuntu 18.04. https://terokarvinen.com/2018/hello-python3-bash-c-c-go-lua-ruby-java-programming-languages-on-ubuntu-18-04/   
Debian Wiki. Java. https://wiki.debian.org/Java  
Oracle. Javac. https://docs.oracle.com/javase/8/docs/technotes/tools/windows/javac.html 
Tero Karvinen. Final Lab for Linux Palvelimet 2024 Spring. https://terokarvinen.com/2024/arvioitava-laboratorioharjoitus-2024-linux-palvelimet/ 
