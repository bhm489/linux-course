# Kotitehtävä 1 

## Raportin kirjoittaminen 

Raporttia kirjoittaessa on tärkeää pitää mielessä monta eri tekijää, jotka vaikuttavat raportin laatuun. 
Raportissa kielen pitää olla selkeää, muistaa väliotsikot ja pitää huolta että ei ala sepittämään valheita. 
On myös tärkeää kuvata esim. millainen ympäristö oli, mitä komentoja käytit, kauanko aikaa kului tai päästiinkö tavoitteeseen. 

Lähde: https://terokarvinen.com/2006/raportin-kirjoittaminen-4/ 

## Free Software Foundation

Neljä olennaista vapautta: 

1. Vapaus suorittaa ohjelma miten haluat ja mihin haluat. 
2. Vapaus oppia miten ohjelma toimii ja muuttaa sitä. Edellytys päästä lähdekoodiin. 
3. Vapaus jakaa ohjelmasta kopioita auttaakseen muita. 
4. Vapaus jakaa kopioita muunnelluista versioista muille. Toiset voivat hyötyä muutoksistasi.

Lähde: https://www.gnu.org/philosophy/free-sw.html 

## Linux:in asentaminen virtuaalikoneeseen

Aloitin Linuxin asentamisen kannettavalle tietokoneelleni 18.1.2025 Klo. 12.08 syrjäisellä mökillä. 
Koneena oli Lenovo Yoga Pro 7 kannettava tietokone. Mökissä ei ollut Wifi-yhteyttä, joten jaoin mobiilidataa omasta puhelimesta. Verkkoyhteys ei ollut ideaalinen, vaan se oli hidas. 

Heti ensimmäiseksi aloitin debian-live-12.9.0-amd64-xfce.iso asennuksen klo. 12.48 lataamalla netistä haluamani version. Nettiyhteys katkesi klo. 13.16, tämä pysäytti asennuksen hetkellisesti, joka viivästytti asennusaikaa hieman. Asennus oli valmis klo. 14.04

Tietokoneessani oli valmiiksi asennettuna Virtual Box, jonka avasin kun debian-live-12.9.0-amd64-xfce.iso asennus oli valmiina käyttöön. 
Ensimmäiseksi aloitin tekemään uutta virtuaalikonetta. Aukeamasta klikkasin "Machine" kohtaa josta valitsin "New" kohdan. Tähän aukeasi "Virtual machine Name and Operating System" johon syötin nimen virtuaalikoneelle. Tähän aukeamaan en muuttanut muuta, mutta katsoin että tyyppi ja versio oli valittu oikein. Valintana oli valmiiksi "Linux" ja "Debian (64-bit), jotka halusinkin. Sitten klikkasin "next", josta aukesi "Hardware", jossa valitsin perusmuistin kooksi 4MB. Klikattuani taas "next" aukesi "Virtual Hard disk", johon valitsin levyn kooksi 60GB. Seuraavaksi tarkistin "Summary" aukeamasta, että
kaikki tiedot ovat oikein ja valitsin "Finish" suorittaakseen asennuksen loppuun. Virtuaalikoneen asennus onnistui oikein ja uusi virtuaalikone oli nyt nähtävissä virtualboxissa.

Seuraavaksi halusin lisätä juuri asennetun Debian ISO image osaksi virtuaalikonetta. Valitsin juuri lisätyn virtuaalikoneen, sieltä "Storage" ---> "Empty" ja "Choose Virtual Optical Disk File" ja sieltä etsin tiedostoista juuri ladatun Debian tiedoston debian-live-12.9.0-amd64-xfce.iso. Haasteena tässä kohdassa oli löytää oikea tiedosto, mutta löysin sen kuitenkin hetkenpäästä. Painamalla aloita näppäintä aukesi debian virtuaalikone onnistuneesti.

Jatkoin asentamista seuraavana päivänä, koska totesin että verkkoyhteys oli liian hidas. Nyt käytössäni oli toimiva Wifi-yhteys. Avasin Debianin klo. 14.29, ja ensimmäiseksi kokeilin toimiiko selain siellä kunnolla. Se toimi hyvin, jonka jälkeen aloin asentamaan Linuxia. Klikkasin Install Debian, jonka jälkeen aloin täyttämään haluttuja tietoja asennukseen. Kieleksi valitsin American English. Sijainniksi klikkasin Suomea kartalta, jolloin alue ja vyöhyke täyttyivät automaattisesti. Näppäimistön malliksi oli valmiina valittuna Generic 105-key PC, jonka halusin pitää. Näppäimistön kieleksi valitsin Suomen + oletus. Sitten asetin kirjautustiedot ja salasanan. Lopuksi klikkasin asenna näppäintä, josta asennus alkoi. Asennus alkoi klo. 14.41 ja päättyi klo. 14.50 ja nyt minulla oli toimiva linux käytössä virtuaalikoneellani. Tämä kohta kesti 19 minuuttia. 

Lähde: https://terokarvinen.com/2021/install-debian-on-virtualbox/ 

## Lähteet: 
Karvinen Tero: Raportin kirjoittaminen. https://terokarvinen.com/2006/raportin-kirjoittaminen-4/  
Free Software Foundation. What is Free Software?. GNU Operating System. https://www.gnu.org/philosophy/free-sw.html  
Karvinen Tero: Install Debian on Virtualbox - Updated 2024. https://terokarvinen.com/2021/install-debian-on-virtualbox/  
Karvinen Tero: Tehtävänanto: https://terokarvinen.com/linux-palvelimet/   
Download Debian ISO image. https://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/   

