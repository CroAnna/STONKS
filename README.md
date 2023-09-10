
<!--Sav programski kod potrebno je verzionirati u glavnoj **master** grani i **obvezno** smjestiti u mapu Software. Sve artefakte (npr. slike) koje ćete koristiti u vašoj dokumentaciju obvezno verzionirati u posebnoj grani koja je već kreirana i koja se naziva **master-docs** i smjestiti u mapu Documentation.

Nakon vaše prijave bit će vam dodijeljen mentor s kojim ćete tijekom semestra raditi na ovom projektu. Mentor će vam slati povratne informacije kroz sekciju Discussions također dostupnu na GitHubu vašeg projekta. -->

# STONKS - Super tehnologija optimalno naprednih kasa Stonks

👉
<a href="https://drive.google.com/file/d/13aoFGcPRaKiJIIHuqjvnR9d5AhfHIhH9/view?usp=share_link">Link za instalaciju softvera</a>👈

Projekt je rađen u tročlanom timu prema tablicama u nastavku, u Windows Forms tehnologiji i Entity Frameworku.

Pogledajte kako izgleda aplikacija u <a href="https://youtu.be/zolUT7hhwVY">videu</a> 👈🎬

<p align="center">
<img src="https://i.ytimg.com/vi/if-2M3K1tqk/maxresdefault.jpg" height="400px" width="600px"  > </img>
</p>



Projekt se bavi temom uobičajene blagajne kojom se koriste sve današnje trgovine uz nekoliko dodatnih, nesvakidašnjih mogućnosti (npr. face recognition pri prijavi).

Postoje 2 vrste prijavljenih korisnika, zaposlenika trgovine - obični zaposlenik i voditelj trgovine (koji ima mogućnost dodavanja artikala i unosa primke, a te su mogućnosti onemogućene običnome zaposleniku).

Zaposlenici mogu skenirati barkodove artikala ili ih ručno odabirati te se ti artikli dodaju na račun prilikom kupnje. Zaposlenik bira način plaćanja kupca te se dodatne informacije (datum, ime prodavača) automatski zapisuju na račun koji će se moći prikazati u PDF obliku. Ukoliko dođe do neočekivane promjene, zaposlenik može stornirati račun te se stanje artikala u trgovini vraća na ono kao da se kupnja nije nikad ni dogodila.
Naravno, mogu se unijeti novi artikli te se povećati stanje proizvoda na skladištu ukoliko dođe nova primka osiguravajući da će u aplikaciji biti ažurni i točni podaci.

Zaposlenici vide sve artikle i sve račune pa, pošto će ih biti puno, imaju neke opcije naprednog pretraživanja, sortiranja i filtriranja. Na kraju svakog dana moći će se izraditi dnevni izvještaj o prometu kako bi uprava trgovine mogla pratiti glavne podatke o poslovanju trgovine.

Svu dokumentaciju o softveru moguće je pronaći na Wiki dijelu repozitorija. Dijagrami su izrađeni pomoću Visual Paradigma.


## Preduvjeti za pokretanje koda:
Kod pokretanja projekta kroz Visual Studio <b>konfiguracija mora biti na x64</b>, a ne na any cpu.

Kod face recognitiona potrebno je malo sporije pritiskati gumbe radi brzine učitavanja slika te se ponekad ne stignu učitati nego se samo prikažu.
Ovo je općenito napomena kod radnji sa slikama i  kamerom.

Kod registracije nakon pritiska gumba za spremanje slike potrebno je malo pričekati da se slika spremi, a tek onda stisnuti gumb za registraciju kako ne bi došlo do poruke da se slika ne nalazi na računalu jer se nije stigla spremiti. Također, kada se na formi za prijavu licem dohvati npr. neka slika, potrebno je malo pričekati da se ta slika stvarno učita, a ne da se samo prikaže (2-3 sekunde).

Funkcionalnosti s licem općenito bolje funkcioniraju kroz Visual Studio.

ZAHTJEV: računalo MORA imati kameru.



## Projektni tim

Ime i prezime  | Github korisničko ime | 
------------ | --------------------- | 
Ana Škarica   | @CroAnna 
Martin Friščić   | @Fr1k1  
Filip Milohanović  | @fmilohano20 

## Opis domene
<!--Umjesto ovih uputa opišite domenu ili problem koji pokrivate vašim  projektom. Domena može biti proizvoljna, ali obratite pozornost da sukladno ishodima učenja, domena omogući primjenu zahtijevanih koncepata kako je to navedeno u sljedećem poglavlju. Priložite odgovarajuće skice gdje je to prikladno.-->
Naša aplikacija reprezentirat će softversko rješenje za sve tipične aspekte maloprodajne blagajne koja je svim prodavačima potrebna. 
## Specifikacija projekta
<!--Umjesto ovih uputa opišite zahtjeve za funkcionalnošću programskog proizvoda. Pobrojite osnovne funkcionalnosti i za svaku naznačite ime odgovornog člana tima. Opišite buduću arhitekturu programskog proizvoda. Obratite pozornost da bi arhitektura trebala biti višeslojna s odvojenom (dislociranom) bazom podatka koju ćemo za vas mi pripremiti i dati vam pristup naknadno. Također uzmite u obzir da bi svaki član tima treba biti odgovorana za otprilike 3 funkcionalnosti, te da bi opterećenje članova tima trebalo biti ujednačeno. Priložite odgovarajuće dijagrame i skice gdje je to prikladno. Funkcionalnosti sustava bobrojite u tablici ispod koristeći predložak koji slijedi:-->

Oznaka | Naziv | Kratki opis | Odgovorni član tima
------ | ----- | ----------- | -------------------
F01 | Login i registracija | Sustav će omogućiti registraciju novih zaposlenika u sustav i prijavu postojećih. Postoje dvije uloge koje imaju različite ovlasti. Samo voditelj može unositi primku i nove artikle. Postojati će neki od naprednijih koncepata prijave (face recognition, NFC ili nešto slično)  | Martin Friščić
F02 | Prikaz računa | Sustav će omogućiti prikaz svih računa, mogućnost naprednih pretraživanja, filtriranje i grafički prikaz statistike računa.| Ana Škarica
F03 | Prikaz svih artikala | Sustav će omogućiti prikaz svih artikala, mogućnost naprednih pretraživanja, filtriranje i grafički prikaz statistike artikala.  | Martin Friščić
F04 | Izrada računa (narudžbe) | Sustav će omogućiti izradu računa, na račun se može dodati više stavki. Biti će omogućeno dodavanje stavki na račun pomoću bar koda ili QR koda s artikla| Ana Škarica
F05 | Generiranje PDF izvještaja (računa) | Sustav će omogućiti da se računi prikažu u PDF formatu. Ispis će biti dizajniran te će izgledati kao račun u stvarnom životu. | Ana Škarica
F06 | Storniranje računa | Sustav će omogućiti storniranje postojećih računa. | Filip Milohanović
F07 | Dodavanje novog artikla | Sustav će omogućiti korisniku tipa voditelj dodavanje novog artikla te će se moći koristiti QR kod ili barkod sa artikla koji je prethodno generiran  | Martin Friščić
F08 | Unos primke | Sustav će omogućiti korisniku tipa voditelj kreiranje primke. Dodavanje stavki biti će moguće pomoću QR koda ili barkoda. Također će se moći vidjeti jednostavan prikaz popisa primki| Filip Milohanović
F09 | Generiranje izvještaja za dnevni promet | Sustav će omogućiti korisniku da generira dnevni izvještaj o prometu prema primjeru iz stvarnog života | Filip Milohanović

## Tehnologije i oprema
<!--Umjesto ovih uputa jasno popišite sve tehnologije, alate i opremu koju ćete koristiti pri implementaciji vašeg rješenja. Projekti se razvijaju koristeći .Net Framework ili .Net Core razvojne okvire, a vrsta projekta može biti WinForms, WPF i UWP. Ne zaboravite planirati korištenje tehnologija u aktivnostima kao što su projektni menadžment ili priprema dokumentacije. Tehnologije koje ćete koristiti bi trebale biti javno dostupne, a ako ih ne budemo obrađivali na vježbama u vašoj dokumentaciji ćete morati navesti način preuzimanja, instaliranja i korištenja onih tehnologija koje su neopbodne kako bi se vaš programski proizvod preveo i pokrenuo. Pazite da svi alati koje ćete koristiti moraju imati odgovarajuću licencu. Što se tiče zahtjeva nastavnika, obvezno je koristiti git i GitHub za verzioniranje programskog koda, GitHub Wiki za pisanje tehničke i projektne dokumentacije, a projektne zadatke je potrebno planirati i pratiti u alatu GitHub projects. -->

ALATI:

<ul>
<li>Github</li>
<li>Visual Paradigm</li>
<li>Visual Studio (WinForms tehnologija) </li>
<li> Microsoft SSMS</li>
<li>.NET Framework</li>
</ul>



Preuzmite softver na sljedećem linku: https://drive.google.com/file/d/13aoFGcPRaKiJIIHuqjvnR9d5AhfHIhH9/view?usp=share_link

## Kako instalirati?

Nakon što korisnik preuzme instalaciju, folder izgleda ovako:

![image](https://user-images.githubusercontent.com/100686979/214886525-b96e29d4-3ae6-4393-a828-cc16d7237784.png)

Potrebno je ući u folder Debug i tamo pokrenuti neki od ovih fileova:

![image](https://user-images.githubusercontent.com/100686979/214886681-a53aab4b-5abf-4e24-a938-908376a35ea4.png)

Sam proces instalacije izgleda ovako:

![image](https://user-images.githubusercontent.com/100686979/214886942-b2a4580b-e8a4-4111-ad00-99f25f8b1db2.png)

Potrebno je pritisnuti na next

![image](https://user-images.githubusercontent.com/100686979/214887021-5631916a-4ae6-4b78-92c9-39129e64ed37.png)

Opet je potrebno pritisnuti next, instalacija je konfigurirana tako da se napravi mapa na desktopu u kojoj se nalazi .exe file tj. s njim se pokreće sama aplikacija.

![image](https://user-images.githubusercontent.com/100686979/214887509-15e9175f-b0ad-4195-9c37-91daf9e7acc8.png)

Next

Zatim je potrebno dopustiti instalaciju.

Na kraju instalacije dobije se ovaj prozor

![image](https://user-images.githubusercontent.com/100686979/214887624-86293b41-2daa-4a35-9a94-80471e501699.png)

Pritisnite close te aplikaciju možete naći na radnoj površini u mapi STONKS i pokrenuti STONKS.exe

![image](https://user-images.githubusercontent.com/100686979/214887843-fb399248-ff0d-497d-a568-5bc42ab8caf0.png)

NAPOMENA KOD PRVOG POKRETANJA:

Obzirom da se nije moguće prijaviti kao neki od korisnika pomoću lica jer slika još ne postoji potrebno je stisnuti na učitaj sliku iz baze

![image](https://user-images.githubusercontent.com/100686979/214892313-bfe425a1-33c0-455b-b13d-3bc145da75fd.png)

Zatim se javlja pogreška da nema tog korisnika. Nakon toga potrebno se prijaviti pomoću username password autentifikacije:

username: chorvat <br/>
password: 1234

![image](https://user-images.githubusercontent.com/100686979/214896453-d7687d5d-c74d-461d-b9f0-3668f691e544.png)


Kada je prijavljen voditelj chorvat, moguće je registrirati novog korisnika (dodati svoje lice) i tako onda testirati sve druge funkcionalnosti.

![image](https://user-images.githubusercontent.com/100686979/214896510-f731f584-2c4b-4f9d-a48d-adae8dd19da1.png)

Odabirom ove opcije može se registrirati novi korisnik pa se onda s njim može prijavljivati licem

![image](https://user-images.githubusercontent.com/100686979/214897050-d3449628-9dbd-4b78-ade8-63e5ed73ca4b.png)

NAPOMENA: uoči testiranja prijave i registracije licem uočeno je da se u rijetkim slučajevima dešava nepoznat bug kod kojeg se ne želi prijaviti korisnik nego baca neki error. Tada je potrebno obrisati aplikaciju, instalirati ju i prijaviti se licem s novim korisnikom.
USPOSTAVLJENO JE DA SE TA GREŠKA JAVLJA KADA SE PREBRZO KLIKA NA OPCIJE JER SE NPR. SLIKA NE STIGNE UČITATI. Također se nakon registracije preporuča pritisnuti na gumb povratak, a ne odmah zatvoriti aplikaciju. Nakon svakog rada s kamerom ili slikom preporučeno je malo pričekati.
Nakon pritiska gumba za spremanje slike na registraciji, potrebno je pričekati neko vrijeme jer je potrebno da se slika spremi na računalo, a tek onda registrirati korisnika kako bi se izbjegla greška da slika ne postoji na računalu jer se ne stigne spremiti. Kod svih operacija sa učitavanjem ili spremanjem slika potrebno je čekati da se slika zapravo spremi/dohvati jer se prikaže prije nego se zapravo dohvati pa onda zna doći do greške. Rješenje je pričekati 3-4 sekunde (vidi se kada se slika promjeni/stvarno spremi na računalo)

<br/>



<br/>

<b> Te greške nikada se ne pojavljuju kroz Visual Studio. Kod svih radnja sa kamerom potrebno je pričekati par sekundi da se radnje stignu izvršiti i ne bi nikada trebalo doći do greške. Znači npr. nakon uključivanja kamere treba pričekati par sekundi i tek onda poslikati i slično. Najkritičnije su operacije spremanja/učitavanja slika jer se slika prikaže prije nego se zapravo učita pa je potrebno malo pričekati. Ako se neprestano javlja error o dretvama, treba reinstalirati aplikaciju. U 30 instalacija se dogodilo samo jednom pa je ovo samo napomena. </b>

## Deinstalacija programa

Kako bi se program deinstalirao, potrebno je otići na upravljačku ploču:
<br/>

![image](https://user-images.githubusercontent.com/100686979/214905654-3e9c190a-441a-44ba-90c2-1509aefbb966.png) <br/>
Odabrati ovu opciju i pritisnuti Uninstall a program.

Zatim je potrebno pronaći STONKS aplikaciju:
![image](https://user-images.githubusercontent.com/100686979/214905806-7bfe29c1-52e7-4e9a-bc79-3665a66cb6e5.png) <br/>

, odabrati ju i stisnuti Uninstall/deinstaliraj ovisno o jeziku

![image](https://user-images.githubusercontent.com/100686979/214905939-007bc1df-dd06-477f-b788-345050207897.png)

Aplikacija će se tada deinstalirati.


# 1. O projektu
## 1.1. Metodološki pristup

Programski tim se odlučio da bi za ovaj projekt bilo najjednostavnije koristiti inkrementalni i bottom-up pristup. <br/>
Inkrementalni će se koristiti pošto omogućuje iterativan rad i poboljšanje funckionalnost, a bottom-up pristup će se koristiti da smanji redundaciju i ubrza rad u programskom timu. <br/>


## 1.2. Terminski plan projekta

Faza razvoja | Opis | Rok |
------------  | ------------------- | ----- |
Analiza poslovne logike | Identificiranje i analiziranje procesa i aktivnosti koji su potrebni za izradu programskog rješenja| 26.10.2022 |
Dizajn softverske arhitekture | Izrada modela koji opisuju arhitekturu i rad samog programskog rješenja | 28.11.2022 |
Dizajn korisničkog sučelja | Izrada skica programskog sučelja | 28.11.2022 |
Implementacija programskog proizvoda | Izrada programskog riješenja i popratne infrastrukture | 23.01.2023 |

*Termini za izradu pojedinih funkcionalnosti se nalaze na GITHUB PROJECTS stranici 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/Gantogram.png"/>

## 1.3. Zaduženja članova tima
Ime i prezime | E-mail adresa (FOI) | JMBAG | Github korisničko ime | Zaduženja |
------------  | ------------------- | ----- | --------------------- | --------- |
Ana Škarica | askarica20@student.foi.hr | 0016147364 | askarica20 | Izrada računa, Prikaz računa, Generiranje PDF izvještaja (računa) |
Martin Friščić | mfriscic20@student.foi.hr | 0016147114 | mfriscic20 | Login i registracija, Dodavanje novog artikla, Prikaz svih artikala |
Filip Milohanović | fmilohano20@student.foi.hr | 0016148270 | fmilohano20 | Unos primke, Storniranje računa, Generiranje izvještaja za dnevni promet |
## 1.4. Izračun troškova

Troškovi izrade STONKS softvera se mogu podijeliti u par različitih kategorija:
1. Analiza poslovne logike
2. Dizajn softverske arhitekture
3. Dizajn korisničkog sučelja
4. Implementacija programskog proizvoda

Za Analizu poslovne logike procijenjeno je da će biti potrebno 30 sati. <br/>
Za Dizajn softverske arhitekture procijenjeno je da će biti potrebno 30 sati. <br/>
Za Dizajn korisničkog sučelja procijenjeno je da će biti potrebno 20 sati. <br/>
Za Implementacija programskog proizvoda procijenjeno je da će biti potrebno 220sati. <br/>

Znači za cijelokupnu izradu programsko riješenja biti će potrebno 300 sati. <br/>
Procijenili smo da su nam ljudski resursi najveći trošak tijekom ovog projekta, pošto je dogovorena satnica 20 eura. <br/>
Nema ostalih značajnih troškova pa je to zanemarivo. <br/>
<br/>
**Iz toga možemo zaključiti da ce nas izrada STONKS programskog rjesenja koštati 6000 eura.** <br/>

## 1.5. Ponuda naručitelju

Naručitelj STONKS proizvoda je trgovački lanac Ducan d.o.o. <br/>
<br/>
Naručitelj planira koristiti STONKS sustav kasa u svim svojim prodavaonicama. <br/>
Pošto se radi o velikom broju poslovnica dogoovrena je prodajna cijena cijena od 75 eura po poslovnica. <br/>
**Ducan ima 600+ poslovnica tako da je kranja cijena softvera (bez PDV-a) 45.000,00 eura.** <br/>
*Cijena edukacije nije uračunata u prodajnu cijenu, može se dogovriti kasnijim ugovorom.

[PDF ponude naručitelju](https://github.com/CroAnna/STONKS/blob/master/Documentation/ponuda_narucitelju.pdf)


# 2. Specifikacija korisničkih softverskih zahtjeva

## 2.1. UVOD
### 2.1.1. Svrha
Ovaj dokument predstavlja specifikaciju zahtjeva za sve tipične aspekte maloprodajne blagajne koja je svim prodavačima potrebna. Skupina osoba kojima je dokument namijenjen su zaposlenici trgovine, koji će se služiti softverom i koji zadaju specifikacije zahtjeva, projekt menadžeri koji su zaduženi za upravljanje izradom softverskog rješenja, programeri i softverski arhitekti koji će prema zahtjevima osmisliti način kako uspješno implementirati softver, ali i testeri koji će isprobati funkcionalnosti softvera i finalan proizvod testirati kako bi se utvrdilo odgovara li rješenje na sve tražene zahtjeve od strane korisnika i funkcionira li na ispravan način. Osim toga, u ovome se dokumentu specificiraju zahtjevi od strane naručitelja (trgovina) i izvođača (poduzeće koje izrađuje softver) pa dokument ima i ulogu svojevrsnog ugovora između navedenih dviju strana. 

### 2.1.2. Opseg
Zaposlenici trgovine mogu prodavati proizvode na tradicionalni, zastarjeli način – pisanjem računa rukom. Zbog navedenog problema poslovanje ne napreduje i trgovina se ne može širiti. Upravo iz tog razloga želi se ubrzati navedeni postupak te cijeli postupak nabave, skladištenja, proučavanje statistike poslovanja i prodaje proizvoda osuvremeniti te čak uvesti i moderne tehnologije poput sustava prepoznavanja lica. Automatizacija procesa nabave i prodaje proizvoda korištenjem softvera smanjit će učestalost ljudskih grešaka, primjerice krivog zbrajanja cijena (ukoliko prodavač upiše krivi broj u kalkulator). Samim time, zaposlenici će biti brži, kupci zadovoljniji te će se broj kupaca po jedinici vremena povećati što će potencijalno rezultirati većim brojem kupaca i rastom poslovanja trgovine. 

Upravo iz tog razloga bi softver, nazvan STONKS (hrv. Super tehnologija optimalno naprednih kasa Stonks), koja prati sustav nabavljanja i prodaje proizvoda te evidentira cjelokupno poslovanje bio izrazito koristan i uvelike bi ubrzao i unaprijedio kvalitetu poslovanja trgovine. Zaposlenici ne bi trebali obraćati pažnju na banalne stvari poput informacije jesu li upisali krivi broj pod šifru proizvoda na računu, nego bi samo skenirati ispravan proizvod, točnije njegov bar kod i cijeli proces bi se automatizirao, a kognitivne sposobnosti proizvođača i ulaganje napora bilo bi svedeno na minimum. Drugim riječima, cjelokupan proces bit će ubrzan i znatno olakšan. 

Ovo rješenje je potpuno novo i značajke su mu da će softver pratiti i evidentirati primku artikala te dodavanje stavki korištenjem barkoda s artikla - kada je primka zaprimljena s osnovnim informacijama o artiklima. Jedino voditelj ima dopuštenje zaprimanja primke (softver ne omogućava svim zaposlenicima trgovine da sami zaprimaju robu), ali i dodavanja novog artikla. Novi artikl će se također moći dodati korištenjem barkoda.
Vrsta prijavljenog zaposlenika bira se pri prijavi u aplikaciju na samome početku te će postojati mogućnost bržeg oblika prijave korištenjem face recognitiona. Svi zaposlenici imat će pristup prikazu svih računa koje će moći pretraživati, filtrirati i sortirati, ali i vidjeti grafički prikaz statistika računa. Iste opcije bit će prisutne i u prikazu artikala. Prilikom dodavanja artikla na račun, što će se moći odraditi ručno, odabirom artikla na ekranu ili putem skeniranja barkoda artikla, bit će moguće dodati više artikala na jedan račun. Unosom svih potrebnih informacija (artikli, količina, način plaćanja) izradit će se račun koji će imati mogućnost generiranja u PDF obliku, ali i storniranja. Osim toga, postojat će i mogućnost generiranja izvještaja za dnevni promet. 

### 2.1.3. Definicije, akronimi i skraćenice

- barkod - način označavanja proizvoda nizom crnih i bijelih linija koje je moguće posebnim uređajima lako optički prepoznati. Koristi se u procesu identifikacije proizvoda, tj.svugdje gdje je potrebno nešto brzo prepoznati

- face recognition - način identifikacije ili potvrđivanja identiteta individualca koristeći njegovo lice te fotografiju njegovog lica pohranjenu u bazi podataka

### 2.1.4. Reference
Nema referenci.

### 2.1.5. Struktura dokumenta
U poglavlju 2 opisana je perspektiva i kontekst softverskog rješenja STONKS, opisuju se funkcije i mogućnosti koje korisnici mogu očekivati od softvera kao i ograničenja o kojima može potencijalno ovisiti sam njegov razvoj. 

U trećemu poglavlju nabrajaju se i objašnjavaju funkcionalni zahtjevi s osnovnim informacijama o njima, a u četvrtome nefunkcionalni, dok su u petome skice sučelja softverskoga rješenja.


## 2.2. OPĆENITI OPIS
### 2.2.1. Perspektiva proizvoda

STONKS je zamišljen kao samostalno rješenje te se u potpunosti kreće od početka u njegovoj izradi, ali imat će interakciju sa bazom podataka. Komunikacija s drugim sustavima nije osmišljena, ali potrebno je naglasiti kako će se u sustavu nalaziti bar kodovi pa će za čitanje barkodova biti potrebno imati neki čitač bar kodova. 

Softversko rješenje će se sastojati od aplikacije za klijenta koja će se izvoditi na računalu krajnjeg korisnika (npr. zaposlenik koji želi izdati račun), a baza bi bila centralizirana kako bi se mogli dijeliti podaci o stanju skladišta. Samo određeni zaposlenici mogu kreirati račun.

Ne koriste se izravno hardverske ni komunikacijske opreme jer je predviđeno da se takvi resursi upotrebljavaju od strane operacijskog sustava.


### 2.2.2. Funkcije proizvoda

- Mogućnost prijave za ovlaštene osobe (zaposlenici neke trgovine gdje treba napraviti neku radnju putem kase)

- Unos artikala s osnovnim informacijama (naziv artikla, cijena artikla, grupa proizvoda...)

- Generiranje računa

- Funkcija pregledavanja dostupnih artikala uz napredne statistike kao što je grafički prikaz

- Funkcija kreiranja PDF izvještaja na temelju računa

- Funkcija prikaza svih računa prema raznim filterima te grafički prikaz statistike računa

- Funkcija ograničavanja pristupa unosa primke i novih artikala (to može samo voditelj)

- Funkcija storniranja postojećih računa

- Mogućnost unosa primke pomoću barkoda ako je zadovoljena uloga.

- Mogućnost prikaza primki

- Izrada i generiranje statističkog izvještaja za dnevni promet



### 2.2.3. Karakteristike korisnika

U osmišljenom softverskom rješenju postoje dvije vrste korisnika, a to su obični zaposlenik koji radi na kasi i voditelj kase koji ima dodatne ovlasti. Zahtijeva se da obje grupe imaju dostatnu razinu obrazovanja i tehničke pismenosti. 

Zaposlenici koriste softver tijekom cijele godine kako bi mogli kontinuirano izdavati račune i zapravo kontrolirati rad cijele trgovine zbog potrebe izrade izvještaja i praćenja statistike dostupnih proizvoda pa do unoštenja artikala i inventure.

Voditelj je svojevrsni upravitelj, tj. administrator softvera te, osim svih mogućnosti zaposlenika, ima i dodatne mogućnosti kao što su izrada raznih statistika, unos primke i dodavanje novog artikla.


### 2.2.4. Ograničenja

Potrebno  je voditi računa o GDPR odredbama za privatnost podataka, a izvođač je dužan da razvoj softvera bude u skladu s dobrim praksama struke te naručitelj ne postavlja dodatna ograničenja u smislu dopuštenih alata i tehnologija izrade. Hardverske karakteristike suvremenih računala su dovoljne za rad sa STONKS softverom te nije potrebno vršiti dodatne investicije i nadogradnje računala. Nije potrebno uvoditi dodatne provjere u svrhu kritičnosti aplikacije pošto se ne upravlja alatima i strojevima koji su potencijalno opasni za korisnike.

### 2.2.5. Pretpostavke i ovisnosti

Ne predviđaju se promjene u tehnologiji i zakonskoj regulativi koje bi mogle utjecati na zahtjeve koji su navedeni u ovome dokumentu, tj. funkcionalnosti kase nije podložan promjenama na toj razini da bi se specifikacijski zahtjevi softvera trebali prilagođavati i mijenjati. Iz tog se razloga ne očekuje promjena na softverskoj razini zahtjeva za STONKS.

### 2.2.6. Ostalo

Nema potrebe za ostalim specifikacijama i dopunskim informacijama o softverskome rješenju.

## 2.3. FUNKCIONALNI ZAHTJEVI 

| Identifikator  | FZ-1 |
| ---      | ---       |
| Zahtjev  | Sustav će omogućiti registraciju novih zaposlenika u sustav i prijavu postojećih. |
| Obrazloženje | Softver radi s artiklima koje trgovina ima na raspolaganju te je potrebno da ovlaštene osobe (zaposlenici trgovina)  imaju mogućnost pristupa podacima, evidenciji i unosu novih podataka. |
| Način provjere | Pokušaj logiranja s ispravnim podacima zaposlenika trgovine rezultira uspješnom prijavom i pristupom pripadajućim funkcionalnostima softvera – voditelj ima sve funkcionalnosti, dok obični zaposlenici trgovine imaju samo određene, dok u ostalim slučajevima neispravnog logiranja rezultat je odbijen pristup podacima u sustavu |
| Prioritet [1-5] | 1 |
| Izvor/Porijeklo | Uprava trgovine |

| Identifikator  | FZ-2 |
| ---      | ---       |
| Zahtjev  | Sustav će omogućiti prikaz svih računa, mogućnost naprednih pretraživanja, filtriranje i grafički prikaz statistike računa. |
| Obrazloženje | Zaposlenici bi trebali u svakom trenutku moći pristupiti popisu računa te ih pretražiti prema određenoj riječi, filtrirati ih te pristupiti grafičkom prikazu statistike izvedene iz podataka s računa |
| Način provjere | Po dolasku na odgovarajući ekran aplikacije popis postojećih računa treba biti vidljiv na ekranu s informacijama o njima te interaktivnih gumbi kojima se mijenja prikaz popisa računa ovisno o željenim i odabranim parametrima prikaza |
| Prioritet [1-5] | 2 |
| Izvor/Porijeklo | Uprava trgovine |


| Identifikator  | FZ-3 |
| ---      | ---       |
| Zahtjev  | Sustav će omogućiti prikaz svih artikala, mogućnost naprednih pretraživanja, filtriranje i grafički prikaz statistike artikala. |
| Obrazloženje | Zaposlenici bi trebali u svakom trenutku moći pristupiti popisu artikala te ih pretražiti prema određenoj riječi, filtrirati ih te pristupiti grafičkom prikazu statistike |
| Način provjere | Po dolasku na odgovarajući ekran aplikacije popis postojećih artikala treba biti vidljiv na ekranu s informacijama o njima te interaktivnih gumbi kojima se mijenja prikaz popisa artikala ovisno o željenim i odabranim parametrima prikaza |
| Prioritet [1-5] | 1 |
| Izvor/Porijeklo | Uprava trgovine |

| Identifikator  | FZ-4 |
| ---      | ---       |
| Zahtjev  | Sustav će omogućiti izradu računa. |
| Obrazloženje | Zaposlenici bi trebali u svakom trenutku moći izraditi račun za kupca temeljem odabranih artikala, automatski dobavljenih podataka o zaposleniku, datumu i načinu plaćanja u svrhu zakonski legalne kupnje te kako bi se moglo zabilježiti novo stanje artikala u trgovini. |
| Način provjere | Unesene promjene o stanju artikala na skladištu trebaju biti pohranjene u sustavu i vidljive svim zaposlenicima. |
| Prioritet [1-5] | 1 |
| Izvor/Porijeklo | Uprava trgovine |

| Identifikator  | FZ-5 |
| ---      | ---       |
| Zahtjev  | Sustav će omogućiti da se računi prikažu u PDF formatu. |
| Obrazloženje | Zaposlenici bi trebali moći isprintati generirani račun u vizualno razumljivom obliku kupcu. Iz tog razloga koristit će se PDF prikaz dokumenta kako bi ga prodavač mogao isporučiti kupcu nakon uspješno provedenog plaćanja kao potvrdu kupnje. |
| Način provjere | Račun se treba uspješno prikazati u PDF obliku, prema standardiziranom dizajnu računa. |
| Prioritet [1-5] | 4 |
| Izvor/Porijeklo | Uprava trgovine |

| Identifikator  | FZ-6 |
| ---      | ---       |
| Zahtjev  | Sustav će omogućiti storniranje postojećih računa. |
| Obrazloženje | Zaposlenici bi trebali moći stornirati račun u svrhu njegova poništavanja. |
| Način provjere | Račun se treba uspješno stornirati te se stanje artikala u trgovini treba vratiti na stanje kao što bi bilo da se kupnja, čiji se račun stornirao, nije nikad dogodila. |
| Prioritet [1-5] | 4 |
| Izvor/Porijeklo | Uprava trgovine |

| Identifikator  | FZ-7 |
| ---      | ---       |
| Zahtjev  | Sustav će omogućiti korisniku tipa voditelj dodavanje novog artikla. |
| Obrazloženje | Voditelj bi trebao moći dodati novi artikl u sustav trgovine kako bi se mogli prodati novi artikli koji dotad nisu postojali u trgovini. |
| Način provjere | Zaposlenik koji ima ulogu voditelja smije imati pristup dodavanju artikla, dok ostalima to treba biti onemogućeno. Nakon uspješnog unosa prikazuje se poruka o uspješnom unosu te se artikl prikazuje u popisu dostupnih artikala. |
| Prioritet [1-5] | 1 |
| Izvor/Porijeklo | Uprava trgovine |

| Identifikator  | FZ-8 |
| ---      | ---       |
| Zahtjev  | Sustav će omogućiti korisniku tipa voditelj kreiranje primke.  |
| Obrazloženje | Voditelj bi trebao moći dodati novu primku u sustav trgovine kako bi se obnovilo stanje skladišta te dostupni artikli i njihove količine.  |
| Način provjere | Zaposlenik koji ima ulogu voditelja smije imati pristup unosu primke, dok ostalima to treba biti onemogućeno. Nakon uspješnog unosa prikazuje se poruka o uspješnom unosu te se količina i vrsta artikla na skladištu obnavlja te se prikazuju novi, aktualni podaci. |
| Prioritet [1-5] | 1 |
| Izvor/Porijeklo | Uprava trgovine |

| Identifikator  | FZ-9 |
| ---      | ---       |
| Zahtjev  | Sustav će omogućiti korisniku da generira dnevni izvještaj o prometu.  | 
| Obrazloženje | Uprava zahtjeva mogućnost generiranja izvještaja o dnevnom prometu kako bi se lakše pratili podaci o dnevnom prometu trgovine u svrhu praćenja rada te lakših donošenja odluka o poslovanju.  |
| Način provjere | Na popisu trebaju biti prikazani svi podaci o dnevnom prometu trgovine. | <!-- FILIP DODAJ TU KAJ SE SVE DOGADA --> 
| Prioritet [1-5] | 5 |
| Izvor/Porijeklo | Uprava trgovine |

## 2.4. NEFUNKCIONALNI ZAHTJEVI 
### 2.4.1. Izgled softvera
NFZ-1 – Sustav će preko grafičkog sučelja vršiti interakciju s korisnicima.

NFZ-2 – Sustav će imati grafičko sučelje s formalnim stilom.

### 2.4.2. Upotrebljivost softvera
NFZ-3 - Sustav će osigurati brzi unos artikla koristeći skeniranje

### 2.4.3. Performanse softvera
NFZ-4 - Sustav će biti dostupan svakodnevno 24 sata.

### 2.4.4. Izvođenje softvera i okruženje
NFZ-5 – Sustav je namijenjen za rad s računalima koja imaju instaliran Windows 10 ili noviji operacijski sustav. 

### 2.4.5. Sigurnost i privatnost
NFZ-6 – Sustav se vodi odrednicama GDPR-a zbog rada s privatnim podacima zaposlenicima fakulteta. <br/>
NFZ-7 - Sustav će imati mogućnost prijave pomoću prepoznavanja lica radi bolje sigurnosti

### 2.4.6. Ostalo
Dodatni nefunkcionalni zahtjevi, a da nisu prethodno navedeni, nisu definirani.
https://github.com/CroAnna/STONKS/blob/master/Documentation/ponuda_narucitelju.pdf
## 2.5. SKICE ZASLONA
### 2.5.1. Skica zaslona za prijavu u sustav
![Slika 1](https://github.com/CroAnna/STONKS/blob/master/Documentation/Prijava.png)

### 2.5.2. Skica zaslona za početni izbornik
![Slika 2](https://github.com/CroAnna/STONKS/blob/master/Documentation/Pocetni_izbornik.png)

### 2.5.3. Skica zaslona za unos artikla
![Slika 3](https://github.comCroAnna/STONKS/blob/master/Documentation/Unos_artikla.png)

### 2.5.4. Skica zaslona za popis svih računa
![Slika 4](https://github.com/CroAnna/STONKS/blob/master/Documentation/Popis_svih_racuna.png)

### 2.5.5. Skica zaslona za ručni unos artikla
![Slika 5](https://github.com/CroAnna/STONKS/blob/master/Documentation/Rucni_unos_artikla.png)

### 2.5.6. Skica zaslona za unos računa
![Slika 6](https://github.com/CroAnna/STONKS/blob/master/Documentation/Unos_racuna.png)

### 2.5.7. Skica zaslona za popis svih artikala
![Slika 7](https://github.com/CroAnna/STONKS/blob/master/Documentation/Popis_svih_artikala.png)

### 2.5.8. Skica zaslona za prijavu
![Slika 8](https://github.com/CroAnna/STONKS/blob/master/Documentation/Prijava.png)

### 2.5.9. Skica zaslona za prijavu pomoću lica
![Slika 9](https://github.com/CroAnna/STONKS/blob/master/Documentation/Prijava_pomocu_lica.png)

### 2.6.1. Skica zaslona za dodavanje fotografije
![Slika 10](https://github.com/CroAnna/STONKS/blob/master/Documentation/Dodavanje_fotografije.png)

### 2.6.2. Skica zaslona za registraciju
![Slika 11](https://github.com/CroAnna/STONKS/blob/master/Documentation/Registracija.png)

### 2.6.3. Skica zaslona za unos primke
![Slika 12](https://github.com/CroAnna/STONKS/blob/master/Documentation/Unos_primke.png)

### 2.6.4. Skica zaslona za prikaz dnevnog prometa
![Slika 13](https://github.com/CroAnna/STONKS/blob/master/Documentation/Dnevni_promet.png)

### 2.6.5. Skica zaslona za dodavanje artikla na račun ručno
![Slika 12](https://github.com/CroAnna/STONKS/blob/master/Documentation/Rucni_unos_artikla.png)

### 2.6.6. Skica zaslona za unos dobavljača
![Slika 12](https://github.com/CroAnna/STONKS/blob/master/Documentation/Unos_dobavljaca.png)



# 3. Dizajn softverskog sustava

## 3.1. Opis slučajeva korištenja i arhitektura
<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/UC%20stonks.svg"/>

## 3.2.1. Specifikacija slučaja korištenja "Prijavljivanje u sustav"
| Login i registracija | FZ-01 |
| --- | --- |
| Kratki opis|Aplikacija će omogućiti da se zaposlenici mogu prijaviti u sustav te će prijava omogućiti pristup svim postojećim funkcionalnostima softverskog rješenja. |
| Sudionici | Zaposlenik trgovine |
| Okidač |Zaposlenik želi upotrebljavati softversko rješenje |
| Iznimke | Nije primjenjivo. |
| Stanje sustava nakon pojave iznimke | Nije primjenjivo. |
| Standardni proces |(1) Zaposlenik zahtijeva pristup softveru, (2) Sustav prikazuje formu za prijavu, (3) Zaposlenik unosi ispravne podatke za prijavu i klikne na gumb, (4) Sustav prikazuje formu za dodatnu autentikaciju pomoću lica, (5) Zaposlenik klikne na gumb za uključivanje kamere, a zatim na prepoznavanje lica, (6) Sustav prepoznaje lice osobe, (7) Zaposlenik klikne na gumb potvrdi ako je ispravno prepoznat, (8) Sustav zatvara formu za prijavu pomoću lica i prikazuje početni izbornik |
| Alternativni proces 1 |(1-2) Isto kao i standardni proces, (3) Zaposlenik unosi neispravne podatke za prijavu i klikne na gumb, (4) Sustav javlja pogrešku o neispravnim podacima, (5) Zaposlenik unosi ispravne podatke, (6-8) Isto kao i standardni proces |
| Alternativni proces 2 |(1) Zaposlenik zahtijeva pristup softveru, (2) Sustav prikazuje formu za prijavu, (3) Zaposlenik unosi ispravne podatke za prijavu i klikne na gumb, (4) Sustav prikazuje formu za dodatnu autentikaciju pomoću lica, (5) Zaposlenik klikne na gumb za prepoznavanje lica, (6) Sustav ne može prepoznati lice jer lice tog korisnika još ne postoji u bazi, (7) Sustav javlja korisniku da ne postoji njegova slika, (8) Korisnik klikne na gumb za dodavanje fotografije, (9) Sustav otvara formu za dodavanje fotografije, (10) Korisnik dodaje vlastitu fotografiju i opet se ide prijaviti, (11) (6-8) iz standardnog procesa |
| Preconditions | Zaposlenik ima pristupne podatke za pristup aplikaciji. |
| Post-conditions |Mogućnost korištenja softvera |

### 3.2.2. Skice ekrana uključenih u "Prijavljivanje u sustav"
<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/Prijava.png"/>
<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/Prijava_pomocu_lica.png"/>
<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/Dodavanje_fotografije.png"/>


### 3.2.3. Dijagram aktivnosti 

Prema uputi prikazana je prijava samo preko face recognitiona.

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/AD%20prijava.svg"/>

### 3.2.4. Dijagram klasa 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/CD%20login%20i%20registracija.svg"/>


## 3.3.1. Specifikacija slučaja korištenja "Registriranje novih zaposlenika"
| Login i registracija | FZ-01 |
| --- | --- |
| Kratki opis| Aplikacija će omogućiti da se u sustav može dodati novi zaposlenik |
| Sudionici | Voditelj trgovine |
| Okidač | Postoji novi zaposlenik koji još nema svoj račun, a treba pristup aplikaciji |
| Iznimke | Nije primjenjivo. |
| Stanje sustava nakon pojave iznimke | Nije primjenjivo. |
| Standardni proces | (1) Voditelj trgovine zahtijeva pristup formi, (2) Sustav prikazuje formu za registraciju, (3) Voditelj unosi podatke o novom zaposleniku, (4) Voditelj klikne na gumb za registriranje korisnika, (5) Sustav javlja poruku o uspješnoj registraciji, (6) Sustav zatvara registracijsku formu i prikazuje formu za prijavu|
| Alternativni proces 1 |(1-2) Isto kao i standardni proces, (3) Voditelj ne unosi neki od obaveznih atributa o zaposleniku kao što je uloga, (4) Sustav javlja poruku pogreške, (5) Voditelj nakon toga unosi točne podatke, (6) Isto kao i standardni proces |
| Alternativni proces 2 |(1-2) Isto kao i standardni proces, (3) Voditelj odabire "Povratak", (4) Sustav zatvara formu bez spremanja podataka |
| Preconditions | Zaposlenik je prijavljen u aplikaciju. Zaposlenik ima ulogu voditelja. |
| Post-conditions | Novi korisnik je registriran u sustav i može se prijaviti|

### 3.3.2. Skice ekrana uključenih u "Registriranje novih zaposlenika"
<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/Registracija.png"/>



### 3.3.3. Dijagram aktivnosti 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/AD%20registracija.svg"/>

### 3.3.4. Dijagram klasa 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/CD%20login%20i%20registracija.svg"/>


## 3.4.1. Specifikacija slučaja korištenja "Unošenje primke"
| Unos primke | FZ-08 |
| --- | --- |
| Kratki opis| Kako bi se zaprimila roba i obnovilo stanje skladišta potrebno je registrirati u sustavu unos artikala. Tu radnju može napraviti jedino voditelj trgovine, dok ostali, obični zaposlenici, nemaju joj pristup. |
| Sudionici | Voditelj trgovine |
| Okidač | Voditelj pristupa formi za unos primke. |
| Iznimke | Nije primjenjivo. |
| Stanje sustava nakon pojave iznimke | Nije primjenjivo. |
| Standardni proces | (1) Zaposlenik zahtijeva pristup formi, (2) Zaposlenik odabire dobavljača, (3) Zaposlenik odabire ručno dodavanje proizvoda, (4) Sustav otvara formu za ručno dodavanje proizvoda, (5) Zaposlenik odabire artikl, (6) Zaposlenik unosi dodatne informacije o artiklu, (7) Zaposlenik odabire "Dodaj artikl" (8) Sustav dodaje artikl u unos računa, (9) Zaposlenik je kliknuo na gumb "Unesi primku", (10) Sustav sprema novu primku s izračunima i ažurira količinu dostupnih artikala, (11) Sustav obavještava korisnika da je primka spremljena, (12) Sustav zatvara formu  |
| Alternativni proces 1 | (1-10) Kao i standardan proces, (8) Sustav javlja da je došlo do pogreške, (9) Sustav zatvara formu |
| Alternativni proces 2 | (1) Zaposlenik zahtijeva pristup formi, (2) Zaposlenik klikom na gumb "Povratak" odustaje od unosa, (3) Sustav zatvara formu |
| Alternativni proces 3 | (1-10) Kao i standardan proces, (11) Zaposlenik je kliknuo na gumb "Odustani", (12) Sustav zatvara formu bez spremanja podataka |
| Preconditions | Zaposlenik je prijavljen u aplikaciju. Zaposlenik ima ulogu voditelja. |
| Post-conditions | Unesena primka i ažurirana količina dostupnih artikala. |

### 3.4.2. Skice ekrana uključenih u "Unošenje primke"
<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/Unos_primke.png"/>

### 3.4.3. Dijagram aktivnosti 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/AD%20Unos%20primke.svg"/>

### 3.4.4. Dijagram klasa 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/CDUnosprimk%20idobavljaca.svg"/>


## 3.5.1. Specifikacija slučaja korištenja "Unošenje dobavljača"
| Unos primke | FZ-08 |
| --- | --- |
| Kratki opis| Kako bi se lakše unijelo primke, potrebno je imati listu dobavljača. Kako bi se mogli dodati novi dobavljači, potrebno je imati i unos dobavljača. |
| Sudionici | Voditelj trgovine |
| Okidač | Voditelj pristupa formi za unos dobavljača. |
| Iznimke | Nije primjenjivo. |
| Stanje sustava nakon pojave iznimke | Nije primjenjivo. |
| Standardni proces | (1) Zaposlenik zahtijeva pristup formi, (2) Zaposlenik unosi podatke o dobavljaču, (3) Zaposlenik odabire "Odustani" (4) Sustav dodaje novog dobavljača, (5) Sustav obavještava korisnika da je dodan dobavljač, (6) Sustav zatvara formu |
| Alternativni proces 1 | (1-4) Kao i standardan proces, (5) Sustav javlja da je došlo do pogreške, (6) Sustav zatvara formu bez spremanja podataka |
| Alternativni proces 2 | (1-2) Kao i standardan proces, (3) Zaposlenik odabire "Odustani", (4) Sustav zatvara formu bez spremanja podataka |
| Preconditions | Zaposlenik je prijavljen u aplikaciju. Zaposlenik ima ulogu voditelja. |
| Post-conditions | |

### 3.5.2. Skice ekrana uključenih u "Unošenje dobavljača"
<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/Unos_dobavljaca.png"/>

### 3.5.3. Dijagram aktivnosti 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/AD%20unos%20dobavljaca.svg"/>

### 3.5.4. Dijagram klasa 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/CDUnosprimk%20idobavljaca.svg"/>







## 3.6.1. Specifikacija slučaja korištenja "Prikazivanje popisa primki"
| Unos primke | FZ-08 |
| --- | --- |
| Kratki opis| Aplikacija će omogućiti da zaposlenici mogu vidjeti primke koje već postoje u sustavu te artikle koji su njima dodani |
| Sudionici | Voditelj trgovine |
| Okidač | Voditelj pristupa formi za unos dobavljača. |
| Iznimke | Nije primjenjivo. |
| Stanje sustava nakon pojave iznimke | Nije primjenjivo. |
| Standardni proces | (1) Zaposlenik zahtijeva pristup formi, (2) Sustav prikazuje sve primke (3) Zaposlenik odabire primku (4) Sustav prikazuje podatke o toj primci u drugoj tablici, (5) Korisnik klikom odabire gumb "Povratak", (6) Sustav zatvara formu  |
| Preconditions | Zaposlenik je prijavljen u aplikaciju. Zaposlenik ima ulogu voditelja.|
| Post-conditions | Prikazane primke i detalji o jednoj odabranoj |


### 3.6.2. Skice ekrana uključenih u "Prikazivanje popisa primki"
<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/PopisPrimki.png"/>

### 3.6.3. Dijagram aktivnosti 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/AD%20Popis%20Primki.svg"/>

### 3.6.4. Dijagram klasa 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/CDUnosprimk%20idobavljaca.svg"/>

## 3.7.1. Specifikacija slučaja korištenja "Izrađivanje novih računa"
| Izrada računa | FZ-04 |
| --- | --- |
| Kratki opis| Kad kupac želi kupiti određene artikle, potrebno je pohraniti artikle i količinu koja se prodaje u sustav, zajedno s ostalim informacijama o plaćanju. Također treba se spremiti račun u sustav, ali i omogućiti spremanje u PDF obliku kako bi kupac imao vlastitu kopiju računa |
| Sudionici | Zaposlenik trgovine |
| Okidač | Zaposlenik pristupa početnoj formi za unos stavaka i izradu računa|
| Iznimke | Nije primjenjivo. |
| Stanje sustava nakon pojave iznimke | Nije primjenjivo. |
| Standardni proces | (1) Zaposlenik zahtijeva pristup formi, (2) Zaposlenik odabire ručno dodavanje proizvoda, (3) Zaposlenik odabire proizvod, (4) Zaposlenik odabire "Dodaj artikl" (5) Sustav dodaje artikl u račun i računa ukupno, (6) Zaposlenik odabire nastavak te se otvara sljedeća forma, (7) Zaposlenik izabire način plaćanja, (8) Odabire izradu računa, (9) Sustav sprema novi račun i ažurira količinu dostupnih artikala te zatvara formu |
| Alternativni proces 1 | (1-7) Kao i standardan proces, (8) Odabire izradu računa s generiranjem PDF-a, (9)  Sustav sprema novi račun, ažurira količinu dostupnih artikala te kreira račun u PDF obliku |
| Alternativni proces 2 | (1) Zaposlenik zahtijeva pristup formi, (2) Zaposlenik klikom na gumb "Odustani" odustaje od unosa novog računa, (3) Sustav zatvara formu bez unosa podataka |
| Alternativni proces 3 | (1-7) Kao i standardan proces, (8) Zaposlenik odabire stavku računa, (9) Zaposlenik klikne na gumb "Izbrisi stavku", (10) Sustav briše odabranu stavku iz računa (11-14) Kao i koraci 6-9 standardnog procesa |
| Alternativni proces 4 | (1-7) Kao i standardan proces, (8) Zaposlenik klikne na gumb "Izbrisi stavku", (9) Sustav obavještava korisnika da ne može obrisati stavku iz računa jer stavka nije odabrana, (10-13) Kao i koraci 6-9 standardnog procesa |
| Alternativni proces 5 | (1-3) Kao i standardan proces, (4) Zaposlenik odabire "Odustani", (5) Sustav zatvara formu te otvara formu Unos računa (6-9) Kao i standardan proces |

| Preconditions | Zaposlenik je prijavljen u aplikaciju. |
| Post-conditions | Unesen novi račun i smanjena količina dostupnih artikala |

### 3.7.2. Skice ekrana uključenih u "Izrađivanje novih računa"
<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/Unos_racuna.png"/>
<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/Rucni_unos_artikla.png"/>
<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/Izrada_racuna.png"/>


### 3.7.3. Dijagram aktivnosti 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/AD%20Izrada%20racuna%20.svg"/>

### 3.7.4. Dijagram klasa 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/CD%20Prikaz%20racuna.svg"/>



## 3.7.1. Specifikacija slučaja korištenja "Izrada izvještaja za dnevni promet"
| Generiranje izvještaja za dnevni promet | FZ-09 |
| --- | --- |
| Kratki opis| |
| Sudionici | Zaposlenik |
| Okidač | Zaposlenik pristupa formi za generiranje izvještaja |
| Iznimke | Nije primjenjivo. |
| Stanje sustava nakon pojave iznimke | Nije primjenjivo. |
| Standardni proces | (1)Zaposlenik zahtijeva pristup formi, (2) Sustav dohvaća sve račune za određeni datum, (3) Sustav računa ukupan iznos sa i bez gotovine i kartica te ukupan promet, (4) Sustav prikazuje izračunate podatke, (5) Korisnik klika "Ispisi promet X", (6) Sustav generira promet X, (7) Sustav zatvara formu |
| Alternativni proces 1 | (1-4) Kao i standardan proces, (5) Korisnik klika "Ispisi promet Z", (6) Sustav generira promet Z, (7) Sustav zatvara formu|
| Alternativni proces 1 | (1-4) Kao i standardan proces, (5) Korisnik klika "Odustani", (6) Sustav zatvara formu|
| Preconditions | Zaposlenik je prijavljen u aplikaciju. |
| Post-conditions | Generiran izvještaj |

### 3.7.2. Skice ekrana uključenih u "Izrada izvještaja za dnevni promet"
<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/Dnevni_promet.png"/>

### 3.7.3. Dijagram aktivnosti 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/AD%20Dnevni%20Promet.svg"/>

### 3.7.4. Dijagram klasa 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/CD%20Dnevni%20promet.svg"/>



## 3.7.1. Specifikacija slučaja korištenja "Prikazivanje svih artikala"
| Prikaz svih artikala | FZ-03 |
| --- | --- |
| Kratki opis| Aplikacija će omogućiti da zaposlenici mogu vidjeti artikle koji već postoje u sustavu, pretražiti ih te vidjeti jednostavnu statistiku o njima|
| Sudionici | Zaposlenik trgovine |
| Okidač | Zaposlenik pristupa popisu artikala |
| Iznimke | Nije primjenjivo. |
| Stanje sustava nakon pojave iznimke | Nije primjenjivo. |
| Standardni proces | (1) Zaposlenik zahtijeva pristup formi, (2) Sustav prikazuje artikle i statistiku o njima, (3) Zaposlenik klikne na gumb "Povratak", (4) Sustav zatvara formu|
| Alternativni proces 1 |(1-2) Isto kao i standardni proces, (3) Zaposlenik klikne na gumb "Povratak", (4) Sustav zatvara formu |
| Alternativni proces 2 |(1-2) Isto kao i standardni proces,  (4) Zaposlenik odabire filter, (5) Sustav prikaže artikle prema odabranome filteru, (6) Zaposlenik klikne na gumb "Povratak", (7) Sustav zatvara formu |
| Alternativni proces 3 |(1-2) Isto kao i standardni proces,  (4) Zaposlenik klikne na gumb "Dodaj artikl", (5) Sustav prikaže formu za dodavanje artikla, (6) Sustav dodaje artikl preko forme, (7) Sustav zatvara formu |
| Preconditions | Zaposlenik je prijavljen u aplikaciju. |
| Post-conditions |Prikazani podaci o artiklima |

### 3.7.2. Skice ekrana uključenih u "Prikazivanje svih artikala"
<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/Popis_svih_artikala.png"/>

### 3.7.3. Dijagram aktivnosti 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/AD%20Prikaz%20artikala.svg"/>

### 3.7.4. Dijagram klasa 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/CD%20unos%20i%20prikaz%20artikla.svg"/>


## 3.7.1. Specifikacija slučaja korištenja "Prikazivanje postojećih računa"
| Prikaz računa| FZ-02 |
| --- | --- |
| Kratki opis| Aplikacija će omogućiti da zaposlenici mogu vidjeti prethodno kreirane račune, pretražiti ih te vidjeti jednostavnu statistiku o njima. Osim toga mogu i stornirati postojeći račun. |
| Sudionici | Zaposlenik trgovine |
| Okidač | Zaposlenik pristupa popisu računa |
| Iznimke | Nije primjenjivo. |
| Stanje sustava nakon pojave iznimke | Nije primjenjivo. |
| Standardni proces | (1) Zaposlenik zahtijeva pristup formi, (2) Sustav prikazuje račune i statistiku o njima, (3) Zaposlenik odabire redak tablice računa, (4) Sustav prikazuje u drugoj tablici stavke odabranog računa, (5) Zaposlenik klikne na gumb "Povratak", (6) Sustav zatvara formu |
| Alternativni proces 1 | (1-3) Kao i standardan proces, (4) Zaposlenik klikne na gumb "Storniraj", (5) Sustav stornira odabrani račun i ažurira stanje dostupnih artikala, (5) Zaposlenik klikne na gumb "Povratak", (6) Sustav zatvara formu |
| Alternativni proces 2 | (1-3) Kao i standardan proces, (4) Zaposlenik odabire filter, (5) Sustav prikaže račune prema odabranome filteru, (6) Zaposlenik klikne na gumb "Povratak", (7) Sustav zatvara formu |
| Alternativni proces 3 | (1-2) Kao i standardan proces, (3) Zaposlenik klikne na gumb "Storniraj", (5) Sustav obavještava korisnika da ne može stornirati račun jer nije odabran, (6) Zaposlenik klikne na gumb "Povratak", (7) Sustav zatvara formu |
| Alternativni proces 4 | (1-2) Kao i standardan proces, (3) Zaposlenik klikne na gumb "Generiraj PDF", (5) Sustav obavještava korisnika da ne može generirati PDF račun jer nije odabran, (6) Zaposlenik klikne na gumb "Povratak", (7) Sustav zatvara formu |
| Alternativni proces 5 | (1-3) Kao i standardan proces, (4) Zaposlenik klikne na gumb "Generiraj PDF", (5) Sustav generira PDF kopiju računa, (6) Zaposlenik klikne na gumb "Povratak", (7) Sustav zatvara formu |
| Preconditions | Zaposlenik je prijavljen u aplikaciju. |
| Post-conditions | Prikazani podaci o računima |

### 3.7.2. Skice ekrana uključenih u "Prikazivanje postojećih računa"
<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/Prikaz_racuna.png"/>

### 3.7.3. Dijagram aktivnosti 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/AD%20Prikaz%20racuna.svg"/>

### 3.7.4. Dijagram klasa 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/CD%20Prikaz%20racuna.svg"/>




## 3.7.1. Specifikacija slučaja korištenja "Unošenje novog artikla"
|Dodavanje novog artikla| FZ-07 |
| --- | --- |
| Kratki opis|Sustav mora omogućiti dodavanje novog artikla pošto su artikli ključni za poslovanje trgovina |
| Sudionici | Zaposlenik trgovine |
| Okidač |Zaposlenik pristupa formi za unos artikla |
| Iznimke | Nije primjenjivo. |
| Stanje sustava nakon pojave iznimke | Nije primjenjivo. |
| Standardni proces |(1) Zaposlenik zahtijeva pristup formi, (2) Zaposlenik unosi podatke o artiklu, (3) Zaposlenik odabire "Dodaj artikl" (4) Sustav dodaje novi artikl, (5) Sustav obavještava korisnika da je dodan artikl, (6) Sustav zatvara formu |
| Alternativni proces 1 |(1-3) Kao i standardan proces, (4) Sustav javlja da je došlo do pogreške, (5) Sustav zatvara formu bez spremanja podataka |
| Alternativni proces 2 |(1-2) Kao i standardan proces, (3) Zaposlenik klikne na gumb za povratak, (5) Sustav zatvara formu bez spremanja podataka |
| Preconditions | Zaposlenik je prijavljen u aplikaciju. Zaposlenik ima ulogu voditelja. |
| Post-conditions | |

### 3.7.2. Skice ekrana uključenih u "Unošenje novog artikla"
<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/Unos_artikla.png"/>

### 3.7.3. Dijagram aktivnosti 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/AD%20Unos%20artikla.svg"/>

### 3.7.4. Dijagram klasa 

<img src = "https://github.com/CroAnna/STONKS/blob/master/Documentation/CD%20unos%20i%20prikaz%20artikla.svg"/>


## 3.4. Kompletan dijagram klasa
<img src ="https://github.com/CroAnna/STONKS/blob/master/Documentation/CD%20spojeno.svg"/>


## 3.5. Kompletan model podataka (ERA dijagram)
<img src ="https://github.com/CroAnna/STONKS/blob/master/Documentation/STONKS_ERA.png"/>



