# Maailma kuulee h4

## x)

### Teoriasta käytäntöön pilvipalvelimen avulla

a. Vuokrattu domainnimi osoittaa palvelimeen. Tässä voi hyödyntää myös Github Education pakettia, jossa palvelimen ja domainnimen saa käyttöön ilmaiseksi.

d. Palomuuri asennetaan komennolla: sudo apt-get install ufw. Tämän jälkeen voidaan tehdä reikä palomuuriin porttia varten.

e. Käyttäjälle on tärkeää keksiä hyvä salasana. Käyttäjästä tehdään pääkäyttäjä. 

f. Kaikki palvelimen ohjelmat on päivitettävä. Avataan terminaali, ja SSH- yhteys virtuaalipalvelimella juuri asetetuilla tunnuksilla. 

Lähde: https://susannalehto.fi/2022/teoriasta-kaytantoon-pilvipalvelimen-avulla-h4/  

### Ensimmäiset vaiheet uudessa virtuaalisessa yksityispalvelimessa

    - Muista aina hyvä salasana
    - Vaiheet:
        - luo uusi virtuaalipalvelin
        - palomuuri
        - sudo käyttäjä
        - sulje juuri tili
        - päivitä ohjelmisto
        - aloita käyttö
        - julkinen DNS-nimi NameCheapissa
 
Lähde: https://terokarvinen.com/2017/first-steps-on-a-new-virtual-private-server-an-example-on-digitalocean/

## Laitteeni 
    - Lenovo Yoga Pro 7
    - AMD Ryzen Prosessori

## a) Vuokraa oma virtuaalipalvelin

#### Aloitus 6.2.2025 klo. 17.11 

Vuokratakseni oman virtuaalipalvelimen Upcloudista ensimmäiseksi loin uuden käyttäjän. Server-kohdasta aloin täyttämään palvelimelle haluttuja tietoja.

Loin SSH-avaimen terminaalissa komennoilla:

    - sudo apt-get install openssh-client    
    - ssh-keygen
   
Kopioin SSH avaimen terminaalista ja syötin sen SSH-avaimen kohtaan. 

![image](https://github.com/user-attachments/assets/d93d4656-596e-41a6-9606-8be6ec5d7b42)

Viimeiseksi painoin Deploy, ja sitten vuokraus oli valmis.  

![image](https://github.com/user-attachments/assets/676c1e7f-6bc1-45f0-9ebb-6ca7c0251d58)

#### Lopetus klo. 17.45 Tähän vaiheeseen kului 34 min.

## b) Alkutoimet (palomuuri, root-tunnus kiinni, ohjelmien päivitys)

#### Aloitus klo. 17.50

### Uusi käyttäjä, sudo-oikeudet

Loin uuden käyttäjän, jolle lisäsin sudo oikeudet. 

Komennoilla: 

    - sudo adduser marianne
    - sudo adduser marianne sudo

![image](https://github.com/user-attachments/assets/a497e63f-7f70-45dc-8caa-f17a70ab9f6e)

![image](https://github.com/user-attachments/assets/7b0d82a2-aee1-48a6-a5f7-6dd5aa813550)

![image](https://github.com/user-attachments/assets/dc1a74dc-cebf-414b-8ac4-fd2975975f18)

### Root-tunnuksen lukitseminen

Varmistin, että käyttäjä on lisätty oikein sudo ryhmään, ennenkun lukitsin root- tunnuksen.
Lukitsin root tunnuksen komennoilla: 

    - sudo usermod --lock root
    - sudo rm /root/.ssh -r

![image](https://github.com/user-attachments/assets/c847e4e1-9400-430f-a04b-2bcb277c22aa)

Valmistin, että se on lukittu oikein. 

![image](https://github.com/user-attachments/assets/7259eb36-3689-4b3b-99a5-7eb8e0150f56)

### Palomuuri

Ensiksi päivitin ohjelmat:

    - sudo apt-get update
    
![image](https://github.com/user-attachments/assets/8b70d0bc-a8df-4d35-a55f-531ec219b090)

Sitten asensin palomuurin komennolla:

    - sudo apt-get install ufw
    
![image](https://github.com/user-attachments/assets/4e719d10-907d-4731-bc44-adf41d20183f)

Tein reiän palomuuriin komennoilla: 

    -sudo ufw allow 22/tcp
    -sudo ufw enable
    
![image](https://github.com/user-attachments/assets/f58296a0-0907-43ae-81cc-5606db3dff8f)

### Pakettien päivitys 

Päivitin ohjelmat komennolla:

    - sudo apt-get dist-upgrade. 
    
Päivityksissä kesti noin minuutti. 

![image](https://github.com/user-attachments/assets/ca8d9b44-e997-4541-83a4-e2ad4d953b34)

#### Lopetus klo. 19.35, b vaiheeseen aikaa kului 1.45 h

## c) Asenna weppipalvelin omalle virtuaalipalvelimellesi

#### Aloitus 7.2.2025 klo. 12.05 

Asensin Apachen: 

    -sudo apt-get install apache2
    
Tein reiän palomuuriin komennolla: 

    -sudo utf allow 80/tcp
    
Yksinkertainen teksti, joka näkyisi sivulla: 

    -echo hei nyt on perjantai!
    -echo hei nyt on perjantai! | sudo tee /var/www/html/index.html

![image](https://github.com/user-attachments/assets/f5ce7d81-76ee-4db0-91fb-289b17dc2292)

Tarkastin, että teksti näkyy sivulla oikein: 

![image](https://github.com/user-attachments/assets/7f8b784b-cb42-4636-8635-5ad1017974f6)

#### Lopetus klo. 12.24, tässä vaiheessa kesti 19 min

## Lähteet: 
Susanna Lehto, 14.2.2022. Teoriasta käytäntöön pilvipalvelimen avulla. https://susannalehto.fi/2022/teoriasta-kaytantoon-pilvipalvelimen-avulla-h4/      
Tero Karvinen, 19.9.2017. First Steps on a New Virtual Private Server – an Example on DigitalOcean and Ubuntu 16.04 LTS.    https://terokarvinen.com/2017/first-steps-on-a-new-virtual-private-server-an-example-on-digitalocean/  
