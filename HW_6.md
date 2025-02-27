# Salataampa h6

## Laitteeni 

- Lenovo Yoga Pro 7
- Ryzen 7 Prosessori

## x) Lue ja tiivistä
#### 26.2.2025 Klo. 9:55 

### Let's Encrypt

- Tavoitteena on mahdollistaa HTTPS-palvelimen perustaminen ja selaimeen tulee automaattisesti sertifikaatti näkyviin.
- Prosessin ensimmäiset vaiheet ovat 

### Using an existing, running web server

- Jos käytössä on jo olemassa oleva palvelin, joka toimii portissa 80, http vaihtoehto vaatii myös http.webroot vaihtoehdon. 

### SSL/TLS Strong Encryption: How-To

- SSL konfiguraation pitää sisältää vähintään:

Listen 443
<VirtualHost *:443>
    ServerName www.example.com
    SSLEngine on
    SSLCertificateFile "/path/to/www.example.com.cert"
    SSLCertificateKeyFile "/path/to/www.example.com.key"
</VirtualHost>

Lähde: https://letsencrypt.org/how-it-works/  
https://go-acme.github.io/lego/usage/cli/obtain-a-certificate/index.html#using-an-existing-running-web-server  
https://httpd.apache.org/docs/2.4/ssl/ssl_howto.html#configexample

#### Lopetus 26.2.2025 Klo. 11:14

## a) Let's 

Hankitaan ja asennetaan palvelimelleni ilmainen TLS-sertifikaatti Let's Encryptilta. 

![image](https://github.com/user-attachments/assets/15a4fa91-446b-4427-92ac-345ee5fbe402)


## b) A-rating

Testataan oman sivuni TLS jollain yleisellä laadunvarmistustyökalulla.

## Vapaaehtoinen

Tee webbilomake, jossa käyttäjätunnus ja salasana. 

## Lähteet 
Let's Encrypt. 26.6.2024. How It Works. https://letsencrypt.org/how-it-works/
