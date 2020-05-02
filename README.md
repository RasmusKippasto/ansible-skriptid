# ansibel-skriptid
## Eesmärk
Skriptide eesmärk on Apache2 veebiserveri instaleerimine Wordpressiga
#### git
##### Paigaldamine
```
apt install git -y
```
##### Seadistamine
```
git config --global user.name "Eesnimi Perenimi"
git config --global user.email email@domeen.com
git config --global core.editor nano
```

#### Skriptid
##### apache.yml
*Paigaldab Apache2 paketi*

##### php7.yml
*Paigaldab php7.0, apchge php7.0 mooduli ja php7.0 mysql mooduli paketid*

##### mysql-server5.7.yml
*Paigaldab mysql serveri, loob root kasutaja mysqlis kõikide õigustega ja loob root login faili kausta /root/.my.cnf*
###### mysql server
- Kasutaja: root
- Kasutaja parool: qwerty

#####  pma.yml
*Skript instaleerib phpmyadmin paketi ja teeb php my admini kättesaadavaks veebi lehe kaudu http://local-host/phpmyadmin*

##### wordpress_paigaldus.sh
*Skript tõmbab uusima wordpressi versiooni, pakib selle lahti ja muudab wp-config-sample.php faili*
*Tekkitab wordpressis uue kasutaja ja andmebaasi mida wordpress hakkab kasutama*
###### mysql server
- andmebaas:                  "wordpress"
- andmebaasi kasutaja:        "wordpressuser"
- andmebaasi kasutaja parool: "qwerty"

## Kasutamine
### Skriptide käivitamise järiekord
1. apache2.yml
2. php7.yml
3. mysql-server.yml
4. pma.yml
6. wordpress.yml
### Ligipääsemine
- Wordpressile saab ligi kirjutades url **{serveri IP}/wordpress**
- Myphpadminile saab ligi kirjutades url **{serveri IP}/myphpadmin**
