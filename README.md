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



###C - Apt ja Get

Yksittäisen ohjelmiston asentaminen toteutetaan syöttämällä sudo apt-get install ohjelma ja painamalla tämän jälkeen Enter-näppäintä.
Useamman ohjelmiston asentaminen toteutettaisiin komentomuodolla sudo apt-get install ohjelma ohjelma ohjelma ja niin eteenpäin kunnes halutut ohjelmistot ovat listattuna ja voidaan painaa Enter-näppäintä. 
Eli pelkkä väli halutun ohjelmiston jälkeen riittää erottamaan ne toisistaan asentamista varten.

###D - Tärkeät kansiot

###E - Grep

###F - Esimerkki putkesta

###G - Esimerkki lokeista
