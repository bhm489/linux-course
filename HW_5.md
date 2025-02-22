# Nimekäs h5


## a) Nimi 

#### 13.2.2025 klo. 12:10

Valitsin NameCheap palvelun, josta hankin nimen. Ensiksi tein itselleni tilin sinne ja täytin tarvittavat tiedot. 
Seuraavaksi katsoin olisiko haluamani nimi vapaa. Pelkkä "taipale" ei ollut vapaa, niin valitsin nimeksi "mariannetaipale".
Lisäsin nimen ostoskoriin ja tarkistin, että tiedot olivat oikein.

![image](https://github.com/user-attachments/assets/f82fb375-1c53-4d13-853c-f9d216f29c74)

![image](https://github.com/user-attachments/assets/16abc6bb-2e32-40d3-8416-ee9551ac1b0e)

![image](https://github.com/user-attachments/assets/a8394bc0-da1f-4a20-908b-0153667d7377)

#### Lopetus 13.2.2025 klo. 12:45
 
## b) Based 

#### 17.2.2025 klo. 16:30

Domain list- kohdasta näkyi omat nimet. Muokatakseen nimen asetuksia klikkasin MANAGE --> Advanced DNS 

![image](https://github.com/user-attachments/assets/75e632af-c201-4e98-9ddc-08a72a575617)

![image](https://github.com/user-attachments/assets/d2305440-c94a-4c5d-8d1b-62e0ea0ec7d4)

Laitoin nimen @ ja www osoittamaan haluttuun IP osoitteeseen.  

![image](https://github.com/user-attachments/assets/434f324e-1d22-4c1a-9d7d-291961296fbf)

Kävin katsomassa näkyykö nyt osoitteessa mariannetaipale.com minun aikaisemmin tehty sivu ja teksti, kyllä näkyi. 

![image](https://github.com/user-attachments/assets/46da410b-621b-429d-9c31-bcc5e4ac3cf3)

#### Lopetus 17.2.2025 klo. 16:55

## c) Kotisivu

#### 20.2.2025 klo. 11:30

Avasin micro-editorin komennolla: 

- $ EDITOR=micro sudoedit mariannetaipale.com.conf

![image](https://github.com/user-attachments/assets/c6f45976-c6d1-440c-950b-175e29399624)

Syötin micro-editoriin: 

![image](https://github.com/user-attachments/assets/a069b281-ea77-4c59-9b2b-7bcfeb449797)

Seuraavaksi syötin seuraavat komennot, että konfiguraatio otetaan käyttöön ja apache käynnistyy uudestaan. 

- sudo a2ensite mariannetaipale.com.conf
  
- sudo systemctl restart apache2

![image](https://github.com/user-attachments/assets/8a6be761-0a12-440b-9ecb-60a1ee91c8c5)

![image](https://github.com/user-attachments/assets/cb74b505-768c-4834-87fb-5f42a7765776)

Tämän jälkeen menin katsomaan sivustolla mikä muuttui. Sain virheilmoituksen Forbidden. 

![image](https://github.com/user-attachments/assets/3f56b3be-90da-4138-bd72-12ac6f7b1282)

Tarkastelin error-lokia, että mistä tämä ilmoitus tuli. 

- $ sudo tail var/log/apache2/error.log

![image](https://github.com/user-attachments/assets/7883abd8-0825-4bb6-bdf6-0d3a560c3bc0)

Päättelin, että ryhmällä ei ollut tarvittavia oikeuksia ja lisäsin nämä oikeudet ryhmälle. 
Annoin tälle ugo+x oikeudet. 

- $ chmod ugo+x marianne

![image](https://github.com/user-attachments/assets/ef345fd5-4cbe-4943-a58c-9e1a386db374)

Lähde: https://cets.seas.upenn.edu/answers/chmod.html 

### Sivut 

![image](https://github.com/user-attachments/assets/ea457267-a21a-4197-b0a6-b0a03d2bd3f0)

Avasin micro-editorin ja tein haluaman tekstin, jonka oli tarkoitus näkyä etusivulla. 

![image](https://github.com/user-attachments/assets/011b69ed-bfe4-4658-93ec-d72392e5b54f)

Teksti näkyi onnistuneesti mariannetaipale.com osoitteessa. 

![image](https://github.com/user-attachments/assets/e63ae199-b2d5-4fd4-8ac5-b4da34f64b62)

Sitten tein kaksi muutakin sivua, blog.html ja projects.html

![image](https://github.com/user-attachments/assets/0a2598d2-97d1-4f08-a11f-043a5534c595)

### Tekstit sivuille ja linkitys 

#### Etusivu

![image](https://github.com/user-attachments/assets/11d5a6e1-5b80-4975-b4cc-96a31b06fbd3)

![image](https://github.com/user-attachments/assets/54abc0a8-b9f2-4bab-8de8-1fb9a9c73977)

#### Blogisivu

![image](https://github.com/user-attachments/assets/021454fc-0905-474e-8e23-9724c883b22b)

![image](https://github.com/user-attachments/assets/bdf0f746-09bb-4e80-ae3d-b097e0990be9)


#### Projektisivu

![image](https://github.com/user-attachments/assets/7e1fb464-3c63-4566-b8d7-b9e7e077c6a3)

![image](https://github.com/user-attachments/assets/64a60a2b-e19d-4306-981d-07b6670caa63)

#### Lopetus 20.2.2025 klo. 13:35

## d) Alidomain

#### 22.2.2025 klo. 12:17

Lisäsin kaksi CNAME tietuetta NameCheap palvelussa kohtaan Advanced DNS. CNAME eli "canonical name" tallentaa pisteitä aliasverkkotunnuksesta "ensisijaiseen" verkkotunnukseen. Nämä nimesin cv ja blogi. 

![image](https://github.com/user-attachments/assets/a1573e84-722b-46f1-997c-8a13027c66bc)

Avasin konfiguraatiotiedoston: 

- $ sudo nano /etc/apache2/sites-available/mariannetaipale.com.conf

Tiedostoon lisäsin ServerAlias kohtaan cv.mariannetaipale.com ja portfolio.mariannetaipale.com. 

![image](https://github.com/user-attachments/assets/9810642e-1756-40c5-a8aa-436ecaf72d39)

Asetukset käyttöön ja uudelleen käynnistys komennoilla: 

- $ sudo a2ensite apache2

- $ sudo systemctl restart apache2
  
![image](https://github.com/user-attachments/assets/e72c204a-ae8e-417f-a651-701a89d09bb1)

Seuraavaksi menin katsomaan toimiko alidomainit sivustolla. Toimi, alidomainit avasivat saman sivun kun päädomain. 

![image](https://github.com/user-attachments/assets/037cd277-19db-48b3-af4c-d97130892080)
![image](https://github.com/user-attachments/assets/300e2e4a-8cdc-4010-92a0-eaf268b414c9)

Lähde: https://www.cloudflare.com/learning/dns/dns-records/dns-cname-record/

#### Lopetus 22.2.2025 klo 13:16

## e) host ja dig

# Lähteet: 
CETS Answers. How do I use chmod to change permissions? https://cets.seas.upenn.edu/answers/chmod.html
Cloudflare. What is a DNS CNAME record? https://www.cloudflare.com/learning/dns/dns-records/dns-cname-record/ 
