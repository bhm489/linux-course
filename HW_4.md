# Maailma kuulee

## x)

a. Vuokrattu domainnimi osoittaa palvelimeen. Tässä voi hyödyntää myös Github Education pakettia, jossa palvelimen ja domainnimen saa käyttöö ilmaiseksi.

d. Palomuuri asennetaan komennolla $ sudo apt-get install ufw. Tämän jälkeen voidaan tehdä reikä palomuuriin porttia varten.

e. Käyttäjälle on tärkeää keksiä hyvä salasana. Käyttäjästä tehdään pääkäyttäjä. 

f. Kaikki palvelimen ohjelmat on päivitettävä. Avataan terminaali, ja SSH- yhteys virtuaalipalvelimella juuri asetetuilla tunnuksilla. 

Lähde: https://susannalehto.fi/2022/teoriasta-kaytantoon-pilvipalvelimen-avulla-h4/  

Ensimmäiset vaiheet uudessa virtuaalisessa yksityispalvelimessa

- Muista aina hyvä salasana.
- Vaiheet:
    - luo uusi virtuaalipalvelin
    - palomuuri
    - sudo käyttäjä
    - sulje juuri tili
    - päivitä ohjelmisto
    - aloita käyttö
    - julkinen DNS-nimi NameCheapissa
 
Lähde: https://terokarvinen.com/2017/first-steps-on-a-new-virtual-private-server-an-example-on-digitalocean/

## a. Vuokraa oma virtuaalipalvelin

klo. 17.11 

![image](https://github.com/user-attachments/assets/676c1e7f-6bc1-45f0-9ebb-6ca7c0251d58)

klo. 17.45

## b. Alkutoimet


klo. 17.50

Loin uuden käyttäjän Lisäsin käyttäjälle sudo oikeudet. 
![image](https://github.com/user-attachments/assets/a497e63f-7f70-45dc-8caa-f17a70ab9f6e)
![image](https://github.com/user-attachments/assets/7b0d82a2-aee1-48a6-a5f7-6dd5aa813550)
![image](https://github.com/user-attachments/assets/dc1a74dc-cebf-414b-8ac4-fd2975975f18)

klo. 18.32 

Varmistin että käyttäjä on lisätty oikein sudo ryhmään, ennenkun suljen root- tunnuksen. 
![image](https://github.com/user-attachments/assets/c847e4e1-9400-430f-a04b-2bcb277c22aa)

Suljin root tunnuksen ja valmistin että se on suljettu oikein. 
![image](https://github.com/user-attachments/assets/7259eb36-3689-4b3b-99a5-7eb8e0150f56)

### Tulimuuri

Ensiksi asensin päivityksen ja asennunsin tulimuurin komennolla: Sudo apt-get 
![image](https://github.com/user-attachments/assets/8b70d0bc-a8df-4d35-a55f-531ec219b090)

![image](https://github.com/user-attachments/assets/4e719d10-907d-4731-bc44-adf41d20183f)

![image](https://github.com/user-attachments/assets/f58296a0-0907-43ae-81cc-5606db3dff8f)

### Pakettien päivitys 

Päivitin ohjelmat komennolla: sudo apt-get dist-upgrade. Päivityksissä kesti noin minuutti. 

![image](https://github.com/user-attachments/assets/ca8d9b44-e997-4541-83a4-e2ad4d953b34)


## c. Asenna weppipalvelin omalle virtuaalipalvelimellesi


## d. Omalle julkiselle palvelimellesi uusi Name Based Virtual Host





Lähteet: 
Susanna Lehto, 14.2.2022. Teoriasta käytäntöön pilvipalvelimen avulla. https://susannalehto.fi/2022/teoriasta-kaytantoon-pilvipalvelimen-avulla-h4/  
Tero Karvinen, 19.9.2017. First Steps on a New Virtual Private Server – an Example on DigitalOcean and Ubuntu 16.04 LTS.    https://terokarvinen.com/2017/first-steps-on-a-new-virtual-private-server-an-example-on-digitalocean/  
