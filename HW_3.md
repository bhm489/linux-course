# Hello Web Server

## Name-Based Virtual Host Support

Name-Based Virtual Host perustuu IP-pohjaiseen virtuaalipalvelimen valinta-algoritmiin. Oikean palvelimen nimeä etsitään virtuaalisten isäntien välillä, joilla on paras IP-osoite. On tärkeää ymmärtää, että ensimmäinen askel nimipohjaisessa virtuaaliisäntäresoluutiossa on IP-pohjainen resoluutio. 

Lähde: https://httpd.apache.org/docs/2.4/vhosts/name-based.html  

## Name Based Virtual Hosts on Apache

Yleensä käytössä on vain yksi IP-osoite ja monia verkkosivustoja isännille. Apachen avulla sinulla voi olla useita verkkotunnuksia yhdessä IP-osoitteessa.

Ensimmäinen askel on asentaa web-palvelin ja vaihtaa oletussivusto komennoilla:
$ sudo apt-get -y install apache2
$ echo "Default"|sudo tee /var/www/html/index.html

Lähde: https://terokarvinen.com/2018/04/10/name-based-virtual-hosts-on-apache-multiple-websites-to-single-ip-address/

## Lähteet: 
The Apache Software Foundation 2023: Apache HTTP Server Version 2.4 Documentation: https://httpd.apache.org/docs/2.4/vhosts/name-based.html  
Karvinen, T. 10.4.2018. Name Based Virtual Hosts on Apache – Multiple Websites to Single IP Address. https://terokarvinen.com/2018/04/10/name-based-virtual-hosts-on-apache-multiple-websites-to-single-ip-address/  
