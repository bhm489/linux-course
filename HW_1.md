# Kotitehtävä 1 

## Raportin kirjoittaminen 

Raporttia kirjoittaessa on tärkeää pitää mielessä monta eri tekijää, jotka vaikuttavat raportin laatuun. 
Raportissa kielen pitää olla selkeää, muistaa väliotsikot ja pitää huolta, että ei ala sepittämään. 
On myös tärkeää kuvata esim. millainen ympäristö oli, mitä komentoja käytettiin, kauanko aikaa kului tai päästiinkö tavoitteeseen. 

Lähde: https://terokarvinen.com/2006/raportin-kirjoittaminen-4/ 

## Free Software Foundation

Neljä olennaista vapautta: 

1. Vapaus suorittaa ohjelma miten haluat ja mihin haluat. 
2. Vapaus oppia miten ohjelma toimii ja muuttaa sitä. Edellytys päästä lähdekoodiin. 
3. Vapaus jakaa ohjelmasta kopioita auttaakseen muita. 
4. Vapaus jakaa kopioita muunnelluista versioista muille. Toiset voivat hyötyä muutoksistasi.

Lähde: https://www.gnu.org/philosophy/free-sw.html 

## Uusi virtuaalikone

Aloitin Linuxin asentamisen kannettavalle tietokoneelleni 18.1.2025 Klo. 12.45 syrjäisellä mökillä. 
Koneena oli Lenovo Yoga Pro 7 kannettava tietokone. Mökissä ei ollut Wifi-yhteyttä, joten jaoin mobiilidataa omasta puhelimesta. Verkkoyhteys ei ollut ideaalinen, vaan se oli hidas. 

Heti ensimmäiseksi aloitin debian-live-12.9.0-amd64-xfce.iso asennuksen klo. 12.48 lataamalla netistä haluamani version. Nettiyhteys katkesi klo. 13.16, tämä pysäytti asennuksen hetkellisesti, joka viivästytti asennusta hieman. Asennus oli valmis klo. 14.04. Tietokoneessani oli valmiiksi asennettuna Oracle Virtual Box, jonka avasin kun debian-live-12.9.0-amd64-xfce.iso asennus oli valmiina käyttöön. Ensimmäiseksi aloitin tekemään uutta virtuaalikonetta. Aukeamasta klikkasin "Machine" --> "New". Tästä aukeasi "Virtual machine Name and Operating System", johon syötin nimen kyseiselle virtuaalikoneelle. Tähän aukeamaan en muuttanut muuta, mutta varmistin, että tyyppi ja versio oli valittu oikein. Valintana oli valmiiksi "Linux" ja "Debian (64-bit)". Sitten klikkasin "next", josta aukesi "Hardware", jossa valitsin perusmuistin kooksi 4 MB. Seuraavalla sivulla "Virtual Hard disk" valitsin levyn kooksi 60 GB. Seuraavaksi varmistin yhteenveto aukeamasta, että kaikki tiedot olivat oikein ja viimeistelläkseen asennuksen klikkasin "Finish". Virtuaalikoneen lisääminen onnistui oikein ja uusi virtuaalikone oli nyt nähtävissä virtualboxissa.

## Debian ISO image

Seuraavaksi halusin lisätä juuri asennetun Debian ISO imagen osaksi virtuaalikonetta. Valitsin juuri lisätyn virtuaalikoneen, ja sen tiedoista "Storage" ---> "Empty" --> "Choose Virtual Optical Disk File" ja sieltä etsin tiedostoista juuri ladatun Debian tiedoston debian-live-12.9.0-amd64-xfce.iso. Painamalla aloita - näppäintä aukesi Debian virtuaalikone onnistuneesti. Päätin jatkaa tehtävää seuraavana päivänä, koska nettiyhteyteni ei toiminut kunnolla. 

## Linux asennus

Jatkoin asentamista seuraavana päivänä 19.1.2025. Nyt käytössäni oli toimiva Wifi-yhteys. Avasin Debianin klo. 14.29, ja ensimmäiseksi valitsin etusivun valinnoista Linux Liven, joka avasi haluamani ympäristön. Seuraavaksi kokeilin toimiiko selain kunnolla klikkaamalla "Applications" ja "Web Browser". Se toimi hyvin, jonka jälkeen aloin asentamaan Linuxia. Klikkasin etusivulta Install Debian, jonka jälkeen aloin täyttämään haluttuja tietoja asennukseen. Kieleksi valitsin American English. Sijainniksi klikkasin Suomea kartalta, jolloin alue ja vyöhyke täyttyivät automaattisesti. Näppäimistön malliksi oli valmiina valittuna Generic 105-key PC, jonka valinnan pidin. Näppäimistön kieleksi valitsin Suomi + oletus. Sitten asetin koneelle nimen, ja kirjautumistiedot. Lopuksi klikkasin "Install" näppäintä, josta asennus alkoi. Asennus alkoi klo. 14.41 ja päättyi klo. 14.50 ja nyt minulla oli toimiva linux käytössä virtuaalikoneellani. 

Pääsin tavoitteeseni asentaa linux virtuaalikoneeseen onnistuneesti. 

Lähde: https://terokarvinen.com/2021/install-debian-on-virtualbox/ 

## Lähteet: 
Karvinen Tero: Raportin kirjoittaminen. https://terokarvinen.com/2006/raportin-kirjoittaminen-4/  
Free Software Foundation. What is Free Software? GNU Operating System. https://www.gnu.org/philosophy/free-sw.html 
Karvinen Tero: Install Debian on Virtualbox - Updated 2024. https://terokarvinen.com/2021/install-debian-on-virtualbox/  
Karvinen Tero: Tehtävänanto: https://terokarvinen.com/linux-palvelimet/ 
Download Debian ISO image. https://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/  

