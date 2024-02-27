Tehtävä H2 - Kaikki testit on toteuttu seuraavanlaisella koneella: Windows 10 OS:llä, Google Chrome selaimella ja koneena on toiminut Legion 5 kannettava. 16Gt RAM, AMD Ryzen 7 5800H, NVIDIA Geforce 3070 ja 200GB vapaata levytilaa SSD-levyasemalla.

# H2 - Komentoja ja asennata
# Terminal komentojen lyhyen kertauksen oppimäärä

##Komentoja komentojen perään

###Liikkuminen

Muistettavien komentojen sivulla on erittäin kattava lista komentoja, joiden avulla on mahdollista päästä etenemään tehokkaasti Linuxin terminaali-ympäristössä.
 Lyhyesti liikkumisen voidaan ajatella toteutuvan cd-komennolla, sijainnin tarkistaminen pwd-komennolla ja sijainnissa olevan sisällön tarkistaminen ls-komennolla.

Jo pelkästään nämä antavat hyvät peruslähtökohdat terminaali-ympäristössä toimimiseen.

###Sisällön muodostaminen

Tämän lisäksi on kriittistä osata muodostaa uusia kansioita mkdir-komennolla.

Itse sisällöllisessä tuotannossa on hyvä muistaa nono tai micro kohde kansiossa ja sen jälkeen halutun tiedostonimen ja tyypin muodostaminen. Tällöin pystyy tekstieditorin kautta muodostamaan haluttua materiaalia, halutussa editorissa. 

###Siirtäminen ja uudelleen nimeäminen

Siirtäminen onnistuu mv-komennolla. Tässä on tärkeää huomioida toiminta tapa mv SIIRRETTÄVÄN TIEDOSTON/KANSION NIMI UUDEN KANSION SIJAINTI/.
Uudelleen nimeäminen onnistuu sekin mv-komennolla, mutta tällöin komentoa määrittää mv VANHANIMI UUSINIMI, eli ensin tulee syöttää vanhan kohteen nimi ja sitten uuden. 
Huom! Jos uutta nimeä ei ole olemassa, nimetään vanhan nimen kohdassa oleva tiedosto uuden mukaiseksi

##SUDO

Liikkumiseen liittyvien komentojen lisälsi tärkein käytössä oleva komento, joka mahdollistaa kaikki kriittisimmät toimet.
sudo apt-get update... yleinen päivitys komento
sudo apt-get upgrade... yleinen päivitystarkistus komento
sudo apt-get install ohjelman nimi... yleinen asennus komento
sudoedit muutettava kohde... yleinen muokkaus komento
sudo nano tai micro ja muodostettavan kohteen nimi... yleinen uuden tekstiä sisältävän kohteen muodostus komento

##Loppu huomiot

Linuxissa tarvitaan loppujen lopuksi suhteelisen vähän komentoja, jotta sillä saadaan tehtyä monimutkaisiakin asioita onnistuneesti. 
Isoimmaksi vaikuttajaksi muodostuukin se, että komentoja tulisi osa käyttää oikeissa paikoissa, oikeaan aikaan. Asia joka on ratkaistavissa ainoastaan tekemällä

#H2-asennusta ja testausta


###A - Micro

Micron saa asetettua testikoneelle syöttämällä terminaalissa sudo apt-get install micro.
Asennus vahvistataan syöttämällä y- sitä kysyttäessä. Jos tätä kohtaa ei haluttaisi tehdä manuaalisesti, olisi syötettävä komento sudo apt-get -y install micro.


###B - Laitteisto

![lshw](https://github.com/Andtonyk/h1---Debian/assets/149326156/f0197fdc-0aad-4e45-aa9b-950994ded88c)

Lshw-listaa käytettävän raudan, alkaen alustasta ja muistista. Muisti näkyy VM:lle asetettuna määränä, mutta esimerkiksi prosessorissa näkyy fyysisen koneen prosessori.
Lshw-siis listaa ositukset käyttäen VM:n muodostamaa tietoa ja koneen omaa listattua raudallista tietoa, riippuen mistä se kyseisen tiedon saa.


###C - Apt ja Get

Yksittäisen ohjelmiston asentaminen toteutetaan syöttämällä sudo apt-get install ohjelma ja painamalla tämän jälkeen Enter-näppäintä.
Hankin koneelleni Micro sekä Nano editointiohjelmat.

![micro](https://github.com/Andtonyk/h1---Debian/assets/149326156/6f6714a5-3b34-49ce-9b8b-ef1d243c0f14)

![nano](https://github.com/Andtonyk/h1---Debian/assets/149326156/9586ae46-82c0-4c9a-8b4b-fcd367e917fd)


Useamman ohjelmiston asentaminen toteutettaisiin komentomuodolla sudo apt-get install ohjelma ohjelma ohjelma ja niin eteenpäin kunnes halutut ohjelmistot ovat listattuna ja voidaan painaa Enter-näppäintä. 
Eli pelkkä väli halutun ohjelmiston jälkeen riittää erottamaan ne toisistaan asentamista varten.


###D - Tärkeät kansiot

Alla on listattuna ohjeistuksen mukaisesti kuvatut kansiot sekä niissä oletuksellisesti olevat tiedostot.

/ - Root eli alin mahdollinen taso
![cd root](https://github.com/Andtonyk/h1---Debian/assets/149326156/2c395a3c-62ee-4eaf-b56e-5816354581cf)

/home/ - Ensimmäinen ei juuri kansio
![cd home](https://github.com/Andtonyk/h1---Debian/assets/149326156/1ac1ced8-8480-415b-969c-6b3e865c3a63)

/home/käyttäjä/ - Kansio joka sisältää käyttäjän pohjalta muodostetun kansio rakenteen ja johon pääasiallisesti tietojen ja kansioiden lisääminen kohdistuu
![cd kayttaja](https://github.com/Andtonyk/h1---Debian/assets/149326156/a39c95c2-e23a-49b5-80da-c6e8ba73db91)

/etc/ - Mahdollistaa dynaamisen liikkuvuuden eri kansioiden ja niissä olevien teksti-tiedostojen välillä
![cd etc](https://github.com/Andtonyk/h1---Debian/assets/149326156/2882f88c-9e23-43d4-8e60-bcec52cd81ec)

/media/ - Potentiaalinen kansio muodostettavalle medialle
![cd media](https://github.com/Andtonyk/h1---Debian/assets/149326156/6d3551f7-99c6-4710-b7f3-3fb75724688b)

/var/log/ - Pitää sisällään kaiken muodostuvan lokitus-datan
![cd var log](https://github.com/Andtonyk/h1---Debian/assets/149326156/0c54409c-b594-46bd-a7b2-2d169093280b)


###E - Grep

Esimerkki 1 - journalctl haku, jossa lokitusta rajoitettaisiin termillä "daemon".

![Putki esimerkki](https://github.com/Andtonyk/h1---Debian/assets/149326156/085b2555-c29d-4690-86ef-9f2724fcc827)

Esimerkki 2 -


Esimerkki 3 - 


###F - Esimerkki putkesta

![Putki esimerkki](https://github.com/Andtonyk/h1---Debian/assets/149326156/085b2555-c29d-4690-86ef-9f2724fcc827)

Putki mahdollistaa lisäkomentojen syöttämisen toisen komennon osaksi. Tässä esimerkissä journalctlstä saadaan putkitetun grepin kautta asetettua haullisia rajoittajia.


###G - Esimerkki lokeista
