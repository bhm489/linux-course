# Kotitehtävä 2

Laitteenani oli Lenovon Yoga Pro 7 kannettava tietokone ja käytössä oli toimiva WiFi-yhteys. 

## x) Command Line Basics Revisited 
$-merkki on automaattisesti komentokehotteessa, jota käyttäjän ei itse tarvitse kirjoitaa. Komentokehote on ollut olemassa jo kauan. Se on kätevä, nopea, ja helppo automatisoida. Komentokehotteessa olemme aina hakemistossa. Helpoimmat tekstieditorit ovat pico ja nano. (https://terokarvinen.com/2020/command-line-basics-revisited/?fromSearch=command%20line%20basics%20revisited). On olemassa monia eri komentoja, joista tärkeimmät ja käytetyimmät on hyvä oppia ulkoa.

## a) Micro

Micro editor asennuksen aloitin 25.1.2025 klo. 12.11. Kopioin Githubin micro-editor asennus kohdasta asennukseen tarvittavan osoitteen: "curl https://getmic.ro | bash". Tämän syötin terminaaliin, joka suoritti asennuksen. Onnistuneesta asennuksesta tuli teksti "Micro Installed". Asennus oli valmis klo. 12.18

![Screenshot 2025-01-25 121100](https://github.com/user-attachments/assets/81d39acc-5ec2-4dee-8071-40a5c53590d8)

Lähde: https://micro-editor.github.io/ 

## b) apt

Aloitin tehtävän klo. 12.02. Päätin asentaa ohjelmat, htop, cowsay ja cmatrix. Kaikki kolme ohjelmaa pystyi asentamaan helposti syöttämättä terminaaliin "sudo apt-get install htop cowsay cmatrix". Tehtävä oli valmis klo. 12.28

![Screenshot 2025-01-25 121845](https://github.com/user-attachments/assets/f2173ee2-8562-488e-b888-98fba1917fe9)

![Screenshot 2025-01-25 121927](https://github.com/user-attachments/assets/875d4d9b-3d4b-464f-8754-539f4608b999)

![Screenshot 2025-01-25 122046](https://github.com/user-attachments/assets/25e9efff-9492-4385-91fa-1badd2633abe)

![Screenshot 2025-01-25 122108](https://github.com/user-attachments/assets/fa8029ef-ff05-4a11-aa27-860c1fb30bc9)

Lähde: https://www.geeksforgeeks.org/apt-get-command-in-linux-with-examples/ 

## c) FHS

Aloitin tehtävän klo. 18.15. Tehtävässä pyydetyt kansiot olivat / - Root directory. /home/ - Home directories for all users. /home/maria/ Home directory of user "xxx". /etc/ - System wide settings. /media/ - Removable media. /var/log - System wide logs. (https://terokarvinen.com/2009/command-line-basics-4/#important_directories). Tehtävä oli valmis klo. 19.50

Root directory. Sain näkyviin syöttämällä terminaaliin: ls /  

![Screenshot 2025-01-25 180219](https://github.com/user-attachments/assets/ac258ad7-3899-44cd-84af-c685c05979b2)

Home directories for all users. Syötin komennon: ls /home/, jolla sain tämän näkyviin.

![Screenshot 2025-01-25 180231](https://github.com/user-attachments/assets/5b340162-8277-44e3-b239-6ee750b1eb1e)

Home directory for user "marianne". Tämän sain näkyviin komennolla: ls /home/marianne  

![Screenshot 2025-01-25 180241](https://github.com/user-attachments/assets/34e4b473-c249-4f0a-b44e-016a5cbdc246)

System wide settings. Syötin terminaaliin komennon: ls /etc/ , tästä tuli paljon tietoa kerralla.  

![Screenshot 2025-01-25 180323](https://github.com/user-attachments/assets/d81b90ab-0169-4396-96d8-a9d0cabe5677)

Removable media. Tästä en ole täysin varma menikö minulla oikein, kun syötin ls /media/ niin mitään ei tapahtunut, mutta en ole täysin varma että mitä olisi pitänyt tulla esille. 
System wide logs. Komennolla: ls /var/log/ sain esille viimeiset kansiot.  

![Screenshot 2025-01-25 180400](https://github.com/user-attachments/assets/c903b94c-7896-4832-8690-809583eae262)

Lähde: https://terokarvinen.com/2009/command-line-basics-4/#important_directories 

## d) grep

Aloitin tehtävän 26.1.2025 klo. 11.32. Ensimmäiseksi tein uuden tiedoston tiedoilla persikka, mandariini ja mustikka. Löytääkseen halutun tekstin syötin komennon: grep mandariini testfile2.txt, joka löysi halutun sanan kyseisestä tiedostosta. Tehtävä oli valmis klo. 12.40

![Screenshot 2025-01-26 135724](https://github.com/user-attachments/assets/5c839e7f-8250-4bb3-82ab-0e3f06933b76)

Lähde: https://phoenixnap.com/kb/grep-command-linux-unix-examples 

## e) pipe

Aloitin tehtävän klo. 12.56 ja se oli valmis klo. 13.24. 

![Screenshot 2025-01-26 140207](https://github.com/user-attachments/assets/47d1b45b-9b2c-4c19-84b8-7ff263591054)

Lähde: https://phoenixnap.com/kb/grep-command-linux-unix-examples 

## f) rauta

Aloitin tekemään tehtävää klo. 14.04 ja se oli valmis klo. 14.56 

![Screenshot 2025-01-26 142100](https://github.com/user-attachments/assets/fcfc3c51-a248-4baa-88fd-2c0666abc50a)

Asensin lshw ensimmäiseksi, että saisin listan näkyviin. 

![Screenshot 2025-01-26 142113](https://github.com/user-attachments/assets/36f269d0-f9d9-4436-86cf-c1ab2d3823b9)

Listauksessa on nähtävissä ensimmäisenä H/W path, jolla viitataan laitteiston polkuun. Device kertoo mihin laitteeseen viitataan. Class määrittää laitteen tyypin tai luokan, esim. muisti tai prosessori. Description nimensä mukaisesti antaa lisätietoa laitteesta.  

![Screenshot 2025-01-26 142034](https://github.com/user-attachments/assets/e27675d7-f026-4fb7-b393-9e93dbaf689b)

## Lähteet 
Tero Karvinen: Command Line Basics Revisited. https://terokarvinen.com/2020/command-line-basics-revisited/?fromSearch=command%20line%20basics%20revisited  
GeeksforGeeks. apt-get command in Linux with Examples. 17.6.2024. https://www.geeksforgeeks.org/apt-get-command-in-linux-with-examples/  
Micro-editor. https://micro-editor.github.io/  
Phoenixnap. grep Command in Linux With Examples. 29.2.2024. https://phoenixnap.com/kb/grep-command-linux-unix-examples   
