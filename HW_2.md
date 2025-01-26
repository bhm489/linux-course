# Kotitehtävä 2

## x) Command Line Basics Revisited 
$-merkki on automaattisesti komentokehotteessa, jota käyttäjän ei itse tarvitse kirjoitaa. Komentokehote on ollut olemassa jo kauan. Se on kätevä, nopea, ja helppo automatisoida. Komentokehotteessa olemme aina hakemistossa. Helpoimmat tekstieditorit ovat pico ja nano. (https://terokarvinen.com/2020/command-line-basics-revisited/?fromSearch=command%20line%20basics%20revisited). On olemassa monia eri komentoja, joista tärkeimmät ja käytetyimmät on hyvä oppia ulkoa. 

## a) Micro

Kopioin Githubin micro-editor asennus kohdasta asennukseen tarvittavan osoitteen: " curl https://getmic.ro | bash " Tämän syötin terminaaliin, joka suoritti asennuksen. Onnistuneesta asennuksesta tuli teksti "Micro Installed".
![Screenshot 2025-01-25 121100](https://github.com/user-attachments/assets/81d39acc-5ec2-4dee-8071-40a5c53590d8)

Lähde: https://micro-editor.github.io/ 

## b) APT 

Päätin asentaa ohjelmat, htop, cowsay ja cmatrix. Kaikki kolme ohjelmaa pystyi asentamaan helposti syöttämättä terminaaliin "sudo apt-get install htop cowsay cmatrix". 

![Screenshot 2025-01-25 121845](https://github.com/user-attachments/assets/f2173ee2-8562-488e-b888-98fba1917fe9)

![Screenshot 2025-01-25 121927](https://github.com/user-attachments/assets/875d4d9b-3d4b-464f-8754-539f4608b999)

![Screenshot 2025-01-25 122046](https://github.com/user-attachments/assets/25e9efff-9492-4385-91fa-1badd2633abe)

![Screenshot 2025-01-25 122108](https://github.com/user-attachments/assets/fa8029ef-ff05-4a11-aa27-860c1fb30bc9)

Lähde: https://www.geeksforgeeks.org/apt-get-command-in-linux-with-examples/ 

## c) FHS

Tehtävässä pyydetyt kansiot olivat / - Root directory. /home/ - Home directories for all users. /home/maria/ Home directory of user "xxx". /etc/ - System wide settings. /media/ - Removable media. /var/log - System wide logs. (https://terokarvinen.com/2009/command-line-basics-4/#important_directories). 

Root directory. Sain näkyviin syöttämällä terminaaliin: ls /  
![Screenshot 2025-01-25 180219](https://github.com/user-attachments/assets/ac258ad7-3899-44cd-84af-c685c05979b2)

Home directories for all users. Syötin komennon: ls /home/, jolla sain tämän näkyviin. Ensiksi tämä ei meinannut toimia, mutta tajusin, että se ei toiminut koska olin jättänyt välilyönnin pois ls ja ensimmäisen / välistä. Tajusin tämän kuitenkin aika äkkiä.  
![Screenshot 2025-01-25 180231](https://github.com/user-attachments/assets/5b340162-8277-44e3-b239-6ee750b1eb1e)

Home directory for user "marianne". Tämän sain näkyviin komennolla: ls /home/marianne  
![Screenshot 2025-01-25 180241](https://github.com/user-attachments/assets/34e4b473-c249-4f0a-b44e-016a5cbdc246)

System wide settings. Syötin terminaaliin komennon: ls /etc/ , tästä tuli paljon tietoa kerralla.  
![Screenshot 2025-01-25 180323](https://github.com/user-attachments/assets/d81b90ab-0169-4396-96d8-a9d0cabe5677)

Removable media. Tästä en ole täysin varma menikö minulla oikein, kun syötin ls /media/ niin mitään ei tapahtunut, mutta en ole täysin varma että mitä olisi pitänyt tulla esille. 
System wide logs. Komennolla: ls /var/log/ sain esille viimeiset kansiot.  
![Screenshot 2025-01-25 180400](https://github.com/user-attachments/assets/c903b94c-7896-4832-8690-809583eae262)

Lähde: https://terokarvinen.com/2009/command-line-basics-4/#important_directories 

## d)

Ensimmäiseksi tein uuden tiedoston tiedoilla persikka, mandariini ja mustikka. Löytääkseen haetun tekstin syötin komennon: grep mandariini testfile2.txt joka löysi tämän sanan kyseisestä tiedostosta.  
![Screenshot 2025-01-26 134654](https://github.com/user-attachments/assets/c2d21074-54d5-413e-95df-9897d6c7ad34)

## e)

## f) 

## Lähteet 
Tero Karvinen: Command Line Basics Revisited. https://terokarvinen.com/2020/command-line-basics-revisited/?fromSearch=command%20line%20basics%20revisited  
GeeksforGeeks. apt-get command in Linux with Examples. 17.6.2024. https://www.geeksforgeeks.org/apt-get-command-in-linux-with-examples/
