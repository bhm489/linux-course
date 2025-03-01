# Salataampa h6

## Laitteeni 

- Lenovo Yoga Pro 7
- Ryzen 7 Prosessori

## x) Lue ja tiivistä
#### 26.2.2025 Klo. 9:55 

### Let's Encrypt

- Tavoitteena on mahdollistaa HTTPS-palvelimen perustaminen ja selaimeen tulee automaattisesti sertifikaatti näkyviin.
- Prosessin ensimmäiset vaiheet ovat, että agentti todistaa CA:lle, että verkkopalvelin hallitsee toimialuetta. Sitten agentti voi pyytää, uusia ja peruuttaa kyseisen toimialueen varmenteita.

Lähde: https://letsencrypt.org/how-it-works/  

### Using an existing, running web server

- Jos käytössä on jo olemassa oleva palvelin, joka toimii portissa 80, http vaihtoehto vaatii myös http.webroot vaihtoehdon.
- Hakemistoa tulee palvella julkisesti nimellä tai verkkotunnuksilla, jotta vahvistus voidaan suorittaa.
  
Lähde: https://go-acme.github.io/lego/usage/cli/obtain-a-certificate/index.html#using-an-existing-running-web-server 

### SSL/TLS Strong Encryption: How-To

- SSL konfiguraation pitää sisältää vähintään:

```  
<VirtualHost *:443>  
    ServerName www.example.com  
    SSLEngine on  
    SSLCertificateFile "/path/to/www.example.com.cert"  
    SSLCertificateKeyFile "/path/to/www.example.com.key"
</VirtualHost>
```

Lähde: https://httpd.apache.org/docs/2.4/ssl/ssl_howto.html#configexample

#### Lopetus 26.2.2025 Klo. 11:14

## a) Let's 
##### 1.3.2025 Klo. 12:03

Hankitaan ja asennetaan palvelimelleni ilmainen TLS-sertifikaatti Let's Encryptilta. Ihan ensimmäiseksi menin katsomaan, että toimiiko verkkosivuni. Kyllä toimi.

![image](https://github.com/user-attachments/assets/78499282-3102-4a8c-8b93-470d30ea6417)

Lukosta, jossa rasti voidaan nähdään, että https ei ole vielä käytössä: 

![image](https://github.com/user-attachments/assets/f547cdb6-a6d3-41b6-b433-21004902a868)

Seuraavaksi kirjauduin sisään minun etäpalvelimelle, päivitin ja latasin legon.

![image](https://github.com/user-attachments/assets/8202589a-b07b-48ba-a022-56d627fdb979)

![Screenshot 2025-02-27 124422](https://github.com/user-attachments/assets/b99eb5a8-d633-4261-a0f7-d7acb0f6628f)    

### Testisertifikaatti

Aloin tekemään testipalvelimella testisertifikaattia. 

Ensimmäiseksi tein lego kansion testisertifikaatille.

![image](https://github.com/user-attachments/assets/c8c62ff7-6f1e-44ec-8223-4cbd733e77d3)

Saadakseni testisertifikaatin suoritin komennon: 

```
$ lego
--server=https://acme-staging-v02.api.letsencrypt.org/directory
--accept-tos
--email=mariannetaipale@gmail.com
--domains=mariannetaipale.com --domains="www.mariannetaipale.com"
--http --http.webroot="/home/marianne/public_sites/mariannetaipale.com/"
--path="/home/marianne/lego/certificates/"
--pem
run
```

![image](https://github.com/user-attachments/assets/759199e9-24f5-4afe-80fd-a17b29c77dad)

Tämä onnistui, ja palautui teksti: 

![image](https://github.com/user-attachments/assets/e64076ac-482c-4292-862a-3430a721315c)

Myös lego kansioon tuli sertifikaatti näkyviin: 

![image](https://github.com/user-attachments/assets/56b6039f-6568-4598-884c-36b684894f15)

### Oikea sertifikaatti

Laitoin testisertifikaatin lego-kansion pois käytöstä ja nimesin sen uudestaan. Tämän jälkeen
tein uuden lego kansion oikealle sertifikaatille.

![image](https://github.com/user-attachments/assets/c5567838-917d-4627-8171-ede5459124f7)

Suoritin komennon: 
```
$ lego
--accept-tos
--email=mariannetaipale@gmail.com
--domains=mariannetaipale.com --domains="www.mariannetaipale.com"
--http --http.webroot="/home/marianne/public_sites/mariannetaipale.com/"
--path="/home/marianne/lego/certificates/"
--pem
run
```
![image](https://github.com/user-attachments/assets/3ff22c71-13d3-4cf9-8bd9-333d3acb3145)

Sertifikaation luominen onnistui, ja sain tekstin "Server responded with a certificate." ja Lego-kansiossa näkyi tämä sertifikaatti. 

![image](https://github.com/user-attachments/assets/7b57bdeb-a072-4202-84e8-35d35d501654)

### Sertifikaatti käyttöön Name Based Virtual Host:issa

Seuraavaksi tarkoituksena olisi ottaa otetaan käyttöön sertifikaatti name based virtual host:issa. Ensiksi menin  Virtual Host asetuksiin ja lisäsin sinne asetukset 443-portilla. 

![image](https://github.com/user-attachments/assets/9e9d11af-856c-4049-a1bc-6acfcd50a35f)

Micro editoriin: 

![image](https://github.com/user-attachments/assets/5a49e7d1-ed5c-41e9-a96c-58eb7c5e98e7)

Sitten muutokset käyttöön: 

 - $ sudo systemctl restart apache2
 - $ sudo apache2ctl configtest

![image](https://github.com/user-attachments/assets/2dc80ca1-5561-481b-b1dd-9db627891235)

## Reikä palomuuriin 443/tcp

Tein reiän palomuuriin komennolla:

- $ sudo ufw 443/tcp

Seuraavaksi menin sivustolle katsomaan onko nyt https onnistuneesti käytössä. Kyllä, nyt minulla oli käytössä https omalla verkkosivulla.

![image](https://github.com/user-attachments/assets/40e0b6e2-b6f2-432e-a597-781e7405091c)

#### Lopetus 1.3.2025 klo. 15:15

## b) A-rating
#### 1.3.2025 klo. 15:25

Testataan oman sivuni TLS eli tietoturvaprotokolla jollain yleisellä laadunvarmistustyökalulla.

Valitsin suositellun laadunvarmistustyökalun, SSLLabs. Syötin hostname-kohtaan oman sivuni osoitteen. 

![image](https://github.com/user-attachments/assets/34ca6d97-ee0f-4791-abaa-e562eab4c05a)

Tulokseksi sain seuraavat: 

Sain A-rating eli SSL sertifikaatti on oikein asennettu ja voimassa. 

![image](https://github.com/user-attachments/assets/95dbe0fc-1ee7-4750-aee3-198f507db132)

![image](https://github.com/user-attachments/assets/c3ca7569-6271-4843-ae79-eed41ad6fea1)

Lähde: https://www.cloudflare.com/learning/ssl/transport-layer-security-tls/  
https://www.ssllabs.com/ssltest/index.html  

#### Lopetus 1.3.2025 klo. 15:50

## Lähteet 
Let's Encrypt. 26.6.2024. How It Works. https://letsencrypt.org/how-it-works/  
Lange 2024: Lego: Obtain a Certificate: https://go-acme.github.io/lego/usage/cli/obtain-a-certificate/index.html#using-an-existing-running-web-server  
The Apache Software Foundation 2025: Apache HTTP Server Version 2.4 [Official] Documentation: SSL/TLS Strong Encryption: How-To: https://httpd.apache.org/docs/2.4/ssl/ssl_howto.html#configexample
SSLLabs. SSL Server Test. https://www.ssllabs.com/ssltest/index.html  
Cloudfare. What is TLS (Transport Layer Security)? https://www.cloudflare.com/learning/ssl/transport-layer-security-tls/
