# Salataampa h6

## Laitteeni 

- Lenovo Yoga Pro 7
- Ryzen 7 Prosessori

## x) Lue ja tiivistä
#### 26.2.2025 Klo. 9:55 

### Let's Encrypt

- Tavoitteena on mahdollistaa HTTPS-palvelimen perustaminen ja selaimeen tulee automaattisesti sertifikaatti näkyviin.
- Prosessin ensimmäiset vaiheet ovat
  
Lähde: https://letsencrypt.org/how-it-works/  

### Using an existing, running web server

- Jos käytössä on jo olemassa oleva palvelin, joka toimii portissa 80, http vaihtoehto vaatii myös http.webroot vaihtoehdon.
- Hakemistoa tulee palvella julkisesti nimellä tai verkkotunnuksilla, jotta vahvistus voidaan suorittaa.
  
Lähde: https://go-acme.github.io/lego/usage/cli/obtain-a-certificate/index.html#using-an-existing-running-web-server 

### SSL/TLS Strong Encryption: How-To

- SSL konfiguraation pitää sisältää vähintään:

Listen 443    
<VirtualHost *:443>    
    ServerName www.example.com    
    SSLEngine on    
    SSLCertificateFile "/path/to/www.example.com.cert"    
    SSLCertificateKeyFile "/path/to/www.example.com.key"    
</VirtualHost>    

Lähde: https://httpd.apache.org/docs/2.4/ssl/ssl_howto.html#configexample

#### Lopetus 26.2.2025 Klo. 11:14

## a) Let's 
##### 1.3.2025 Klo. 11:15

Hankitaan ja asennetaan palvelimelleni ilmainen TLS-sertifikaatti Let's Encryptilta. Ihan ensimmäiseksi menin katsomaan, että toimiiko verkkosivuni. Kyllä toimi.

![image](https://github.com/user-attachments/assets/78499282-3102-4a8c-8b93-470d30ea6417)

Lukosta, jossa rasti voidaan nähdään, että https ei ole vielä käytössä: 

![image](https://github.com/user-attachments/assets/f547cdb6-a6d3-41b6-b433-21004902a868)

Seuraavaksi kirjauduin sisään minun etäpalvelimelle, päivitin ja latasin legon.

![image](https://github.com/user-attachments/assets/8202589a-b07b-48ba-a022-56d627fdb979)

![Screenshot 2025-02-27 124422](https://github.com/user-attachments/assets/b99eb5a8-d633-4261-a0f7-d7acb0f6628f)    

Hain sertifikaatin legolla komennolla: 

```
$ lego
--server=https://acme-staging-v02.api.letsencrypt.org/directory
--accept-tos
--email="ishouldchangesamplevalues@example.com"
--domains="tero.example.com" --domains="www.tero.example.com"
--http --http.webroot="/home/tero/public_sites/tero.example.com/"
--path="/home/tero/lego/certificates/"
--pem
run
```


## b) A-rating

Testataan oman sivuni TLS jollain yleisellä laadunvarmistustyökalulla.

## Vapaaehtoinen

Tee webbilomake, jossa käyttäjätunnus ja salasana. 

## Lähteet 
Let's Encrypt. 26.6.2024. How It Works. https://letsencrypt.org/how-it-works/
