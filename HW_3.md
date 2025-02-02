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

Asensin Apache2 ja onnistunut asennus näkyi localhost osoitteessa:  
![Screenshot 2025-01-31 160838](https://github.com/user-attachments/assets/caa3a17d-986c-4f4a-991c-59d18543d7df)  
Tähän kohtaan aikaa kului noin 10 min. 

## Loki

Lokissa näkyvät rivit: 
![image](https://github.com/user-attachments/assets/ec01af9e-046b-4bf5-9e01-71f364eebf0f)

Rivien analysointi: 
1. 127.0.0.1 - Tarkoittaa asiakkaan IP-osoitetta, jolta pyynty tuli. 
2. [31/Jan/2025:14:08:52 + 0200] - Aikaleima, jolloin pyyntö on tehty. 
3. "GET /favicon.ico HTTP/1.1"- HTTP pyyntö. GET - asiakas haluaa ladata sivun. 
4. "http://localhost/" - Tieto mistä sivulta asiakas tuli.
5. 404 - Sivua ei löytynyt palvelimenta, koska sitä ei ole vielä tehty
6. 407 - Virhe
7. "Mozilla/5.0 (XII: Linux x86_64: rv: 128.0) - Käytetään Mozilla selainta

Tässä vaiheessa aikaa kului 45min. 

Lähde: https://www.sumologic.com/blog/apache-access-log/ 

## Etusivu

![image](https://github.com/user-attachments/assets/060c1387-5003-4d75-a889-12b79fafbf3c)

Lähde: https://www.youtube.com/watch?v=jp4UHtnNfgM  

## curl

![image](https://github.com/user-attachments/assets/c453f99b-6244-428e-83c0-84668700b583)


## Lähteet: 
The Apache Software Foundation 2023: Apache HTTP Server Version 2.4 Documentation: https://httpd.apache.org/docs/2.4/vhosts/name-based.html  
Karvinen, T. 10.4.2018. Name Based Virtual Hosts on Apache – Multiple Websites to Single IP Address. https://terokarvinen.com/2018/04/10/name-based-virtual-hosts-on-apache-multiple-websites-to-single-ip-address/ 
Sumo logic. 14.1.2020. Understanding the apache access log: View, Locate, Analyze. https://www.sumologic.com/blog/apache-access-log/
