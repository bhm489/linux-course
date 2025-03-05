# Nimekäs h5

Tekijä: Marianne Taipale   
Kotitehtävä kurssille: Linux Palvelimet ICI003AS2A-3008  
Tehtävänanto: https://terokarvinen.com/linux-palvelimet/   

## Laitteeni
- Lenovo Yoga Pro 7
- Ryzen 7 Prosessori

## a) Nimi 
#### 13.2.2025 klo. 12:10

Valitsin NameCheap palvelun, josta hankin nimen. Ensiksi tein itselleni tilin sinne ja täytin tarvittavat tiedot. 
Seuraavaksi katsoin olisiko haluamani nimi vapaa. Pelkkä "taipale" ei ollut vapaa, niin valitsin nimeksi "mariannetaipale".
Lisäsin nimen ostoskoriin ja tarkistin, että tiedot olivat oikein.

![image](https://github.com/user-attachments/assets/f82fb375-1c53-4d13-853c-f9d216f29c74)

![image](https://github.com/user-attachments/assets/16abc6bb-2e32-40d3-8416-ee9551ac1b0e)

![image](https://github.com/user-attachments/assets/a8394bc0-da1f-4a20-908b-0153667d7377)

### Osoittamaan omaan koneeseen 

Domain list- kohdasta näkyi omat nimet. Muokatakseen nimen asetuksia klikkasin MANAGE --> Advanced DNS 

![image](https://github.com/user-attachments/assets/75e632af-c201-4e98-9ddc-08a72a575617)

![image](https://github.com/user-attachments/assets/d2305440-c94a-4c5d-8d1b-62e0ea0ec7d4)

Laitoin @ ja www osoittamaan haluttuun IP osoitteeseen.  

![image](https://github.com/user-attachments/assets/434f324e-1d22-4c1a-9d7d-291961296fbf)

Kävin katsomassa näkyikö osoitteessa mariannetaipale.com minun aikaisemmin tekemäni sivu ja teksti, kyllä näkyi. 

![image](https://github.com/user-attachments/assets/46da410b-621b-429d-9c31-bcc5e4ac3cf3)
#### Lopetus 13.2.2025 klo. 13:05

## b) Based, Name Based Virtual Host näkymään uudessa nimessä.
#### 17.2.2025 klo. 16:30

Avasin micro-editorin komennolla: 

- $ EDITOR=micro sudoedit mariannetaipale.com.conf

![image](https://github.com/user-attachments/assets/c6f45976-c6d1-440c-950b-175e29399624)

Syötin micro-editoriin: 

![image](https://github.com/user-attachments/assets/a069b281-ea77-4c59-9b2b-7bcfeb449797)

Seuraavaksi syötin seuraavat komennot, että konfiguraatio otetaan käyttöön ja apache käynnistyy uudestaan. 

- $ sudo a2ensite mariannetaipale.com.conf
  
- $ sudo systemctl restart apache2

![image](https://github.com/user-attachments/assets/8a6be761-0a12-440b-9ecb-60a1ee91c8c5)

![image](https://github.com/user-attachments/assets/cb74b505-768c-4834-87fb-5f42a7765776)

Tämän jälkeen menin katsomaan sivustolla mikä muuttui. Sain virheilmoituksen Forbidden. 

![image](https://github.com/user-attachments/assets/3f56b3be-90da-4138-bd72-12ac6f7b1282)

Tarkastelin error-lokia, että mistä tämä ilmoitus tuli. 

- $ sudo tail /var/log/apache2/error.log

![image](https://github.com/user-attachments/assets/7883abd8-0825-4bb6-bdf6-0d3a560c3bc0)

Päättelin, että ryhmällä ei ollut tarvittavia oikeuksia ja lisäsin nämä oikeudet ryhmälle. 
Annoin tälle ugo+x oikeudet. 

- $ chmod ugo+x marianne

![image](https://github.com/user-attachments/assets/ef345fd5-4cbe-4943-a58c-9e1a386db374)

Lähde: https://cets.seas.upenn.edu/answers/chmod.html 
#### Lopetus 17.2.2025 klo. 17:45

## c) Kotisivu
#### 20.2.2025 klo. 11:30

![image](https://github.com/user-attachments/assets/ea457267-a21a-4197-b0a6-b0a03d2bd3f0)

Avasin micro-editorin ja tein haluaman tekstin, jonka oli tarkoitus näkyä etusivulla. 

![image](https://github.com/user-attachments/assets/011b69ed-bfe4-4658-93ec-d72392e5b54f)

Teksti näkyi onnistuneesti mariannetaipale.com osoitteessa. 

![image](https://github.com/user-attachments/assets/e63ae199-b2d5-4fd4-8ac5-b4da34f64b62)

Sitten tein kaksi muutakin sivua, blog.html ja projects.html

![image](https://github.com/user-attachments/assets/0a2598d2-97d1-4f08-a11f-043a5534c595)

### Tekstit sivuille ja linkitys 

### Etusivu

![image](https://github.com/user-attachments/assets/4c210d15-82b9-4b49-948a-9545b8b992d6)

![image](https://github.com/user-attachments/assets/dae7ae5f-649c-43bf-88fb-8382a337882e)

### Blogisivu

![image](https://github.com/user-attachments/assets/bd473d84-6272-4c19-80c2-c3e5a4a740f7)

![image](https://github.com/user-attachments/assets/f3241edd-5cdd-4652-afb2-b6f2798f02ff)

### Projektisivu

![image](https://github.com/user-attachments/assets/32a96a76-5199-43d5-aff5-92719caf6438)

![image](https://github.com/user-attachments/assets/5a6ad005-98ef-4078-9958-dace9c218c29)

#### Lopetus 20.2.2025 klo. 13:35

## d) Alidomain
#### 22.2.2025 klo. 12:17

Lisäsin kaksi CNAME tietuetta NameCheap palvelussa kohtaan Advanced DNS. CNAME eli "canonical name" tallentaa pisteitä aliasverkkotunnuksesta "ensisijaiseen" verkkotunnukseen. Nämä nimesin cv ja portfolio. Lähde: https://www.cloudflare.com/learning/dns/dns-records/dns-cname-record/

![image](https://github.com/user-attachments/assets/a1573e84-722b-46f1-997c-8a13027c66bc)

Avasin konfiguraatiotiedoston: 

- $ sudo nano /etc/apache2/sites-available/mariannetaipale.com.conf

Tiedostoon lisäsin ServerAlias kohtaan cv.mariannetaipale.com ja portfolio.mariannetaipale.com. 

![image](https://github.com/user-attachments/assets/07438bc1-9f69-47cf-be6a-d89ac124740f)

Asetukset käyttöön ja uudelleen käynnistys komennoilla: 

- $ sudo a2ensite apache2

- $ sudo systemctl restart apache2
  
![image](https://github.com/user-attachments/assets/e72c204a-ae8e-417f-a651-701a89d09bb1)

Seuraavaksi menin katsomaan toimiko alidomainit sivustolla. Toimi, alidomainit avasivat saman sivun kun päädomain. 

![image](https://github.com/user-attachments/assets/81c47da1-a555-41fd-84fb-29e78a1b572a)
![image](https://github.com/user-attachments/assets/55738277-00b5-4eaa-adbc-6fe7d6030648)

#### Lopetus 22.2.2025 klo 13:16

## e) host ja dig
#### 22.2.2025 klo. 13:44 

Asensin tarvittavat työkalut. 

- $ sudo apt update
- $ sudo apt install dnsutils -y

![image](https://github.com/user-attachments/assets/c2861ba0-92de-487a-a602-c362e13c20db)

### Oma domain

- $ host mariannetaipale.com
- $ dig mariannetaipale.com ANY
  
![image](https://github.com/user-attachments/assets/3f46eeeb-48ca-46ff-8d80-afc2db73f87a)    

NameCheapin Advanced DNS:  
![image](https://github.com/user-attachments/assets/aa732e95-4590-4f37-b1b5-2c2c5f92aad1)

Terminaalissa host-komento näytti mariannetaipale.com A-tietueen, eli IP osoitteen, joka oli sama kuin NameCheapin Advanced DNS asetuksissa. 
dig-komennolla näkyi paljon enemmän tietoa. Tässä näkyi A tietue (IP-osoite), joka oli sama kuin NameCheapin DNS asetuksissa. Tässä näkyi myös nimipalvelimet(NS) ja sähköpostipalvelin(MX).

### Pienyritys

- $ host kauneusprimavera.fi
- $ dig kauneusprimavera.fi ANY
  
![image](https://github.com/user-attachments/assets/b3eb4323-44cb-4625-b165-68cd0e546529)

Tässä host-komento kertoi pienyrityksen IP-osoitteen, IPv6 osoitteen ja sähköpostipalvelimen. 
dig-komennolla löytyi aika lailla samat tiedot. AAAA eli käytössä IPv6 osoite. 
A tietue eli IP osoite. Sähköpostipalvelimen 10 mail1.sigmatic.fi

### Suuriyritys

- $ host youtube.com
- $ dig youtube.com ANY
  
![image](https://github.com/user-attachments/assets/3d2efa04-9cbd-4f69-97a3-bc3975265d4f)

host-komennolla näkyi IP osoite, IPv6 osoite ja sähköpostipalvelin. dig-komennolla löytyi A tietue eli IP osoite, kaikki nimipalvelimet, sähköpostipalvelin 0 smtp.google.com ja AAAA eli IPv6 osoite.
#### Lopetus 22.2.2025 klo. 14:50 

# Lähteet: 
CETS Answers. How do I use chmod to change permissions? https://cets.seas.upenn.edu/answers/chmod.html   
Cloudflare. What is a DNS CNAME record? https://www.cloudflare.com/learning/dns/dns-records/dns-cname-record/ 
