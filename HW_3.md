# Hello Web Server

Laitteeni:
Lenovo Yoga Pro 7 ja toimiva wifi-yhteys. 
AMD Ryzen 7 prosessori. 

## Name-Based Virtual Host Support

Name-Based Virtual Host perustuu IP-pohjaiseen virtuaalipalvelimen valinta-algoritmiin. Oikean palvelimen nimeä etsitään virtuaalisten isäntien välillä, joilla on paras IP-osoite. On tärkeää ymmärtää, että ensimmäinen askel on IP-pohjainen resoluutio. 

Lähde: https://httpd.apache.org/docs/2.4/vhosts/name-based.html  

## Name Based Virtual Hosts on Apache

Yleensä käytössä on vain yksi IP-osoite ja monia verkkosivustoja isännille. Apachen avulla sinulla voi olla useita verkkotunnuksia yhdessä IP-osoitteessa.

Ensimmäinen askel on asentaa web-palvelin ja vaihtaa oletussivusto komennoilla:  
$ sudo apt-get -y install apache2  
$ echo "Default"|sudo tee /var/www/html/index.html

Lähde: https://terokarvinen.com/2018/04/10/name-based-virtual-hosts-on-apache-multiple-websites-to-single-ip-address/

## Apache asennus 

Asensin Apache2 ja onnistunut asennus näkyi selaimessa http://localhost osoitteessa: 

![Screenshot 2025-01-31 160838](https://github.com/user-attachments/assets/caa3a17d-986c-4f4a-991c-59d18543d7df)  

Tähän kohtaan aikaa kului noin 10 min. 

## Loki

Lokissa näkyvät rivit:   
![image](https://github.com/user-attachments/assets/ec01af9e-046b-4bf5-9e01-71f364eebf0f)

Rivien analysointi:   
1. 127.0.0.1 - Tarkoittaa asiakkaan IP-osoitetta, jolta pyynty tuli. 
2. [31/Jan/2025:16:08:26 + 0200] - Aikaleima, jolloin pyyntö on tehty. 
3. "GET / HTTP/1.1"- HTTP pyyntö joka lähetettiin palvelimelle. GET - asiakas haluaa ladata sivun.
4. 200 - pyyntö onnistui
5. 3380 - tiedoston koko
6. "Mozilla/5.0 (XII: Linux x86_64: rv: 128.0) Gecko/2010 0101 Firefox/128.0"- Kertoo mitä laitetta ja selainta asiakas käyttää.

Tässä vaiheessa aikaa kului 45min. 

Lähde: https://www.sumologic.com/blog/apache-access-log/ 

## Etusivu

Sijoitin HTML tiedoston hakemistoon -- > /var/www/html/index.html. Kirjoitin html koodiin sen mitä halusin näkyvän sivustolla. 
![Screenshot 2025-02-01 102427](https://github.com/user-attachments/assets/b6a995e9-82ff-445a-9ca1-e382449828dc)

Käynnistin apachen uudestaan, että varmasti toimisi --> sudo systemctl restart apache2 
![image](https://github.com/user-attachments/assets/060c1387-5003-4d75-a889-12b79fafbf3c)

Tähän aikaa kului 1.20 h. 

Lähde: https://www.youtube.com/watch?v=jp4UHtnNfgM  

## curl

Curl -I hakee HTTP otsakkeet, ilman itse sivun sisältöä. Pelkkä Curl hakee koko sivun sisällön. Palauttaa koko html-sivun sisällön. 

Curl -I. Muutama otsake selitetty: 

HTTP/1.1 200 OK - tarkoittaa, että pyyntö onnistui. 
Date: Sat, 01 Feb 2025 14:10:57 GMT - Aikaleima, jolloin palvelin vastasi pyyntöön. 
Server: Apache/2.4.62 (Debian) - Kertoo että palvelimena on Apache ja numero kertoo, että mikä versio on käytössä. 

![image](https://github.com/user-attachments/assets/c453f99b-6244-428e-83c0-84668700b583)

Aikaa tähän osaan kului 25min. 

Lähde: https://www.geeksforgeeks.org/curl-command-in-linux-with-examples/

## Lähteet: 
The Apache Software Foundation 2023: Apache HTTP Server Version 2.4 Documentation: https://httpd.apache.org/docs/2.4/vhosts/name-based.html    
Karvinen, T. 10.4.2018. Name Based Virtual Hosts on Apache – Multiple Websites to Single IP Address. https://terokarvinen.com/2018/04/10/name-based-virtual-hosts-on-apache-multiple-websites-to-single-ip-address/   
Sumo logic. 14.1.2020. Understanding the apache access log: View, Locate, Analyze. https://www.sumologic.com/blog/apache-access-log/  
Geeksforgeeks. curl Command in Linux with Examples. 11.4.2024. https://www.geeksforgeeks.org/curl-command-in-linux-with-examples/  
