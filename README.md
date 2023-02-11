
<!--Sav programski kod potrebno je verzionirati u glavnoj **master** grani i **obvezno** smjestiti u mapu Software. Sve artefakte (npr. slike) koje ćete koristiti u vašoj dokumentaciju obvezno verzionirati u posebnoj grani koja je već kreirana i koja se naziva **master-docs** i smjestiti u mapu Documentation.

Nakon vaše prijave bit će vam dodijeljen mentor s kojim ćete tijekom semestra raditi na ovom projektu. Mentor će vam slati povratne informacije kroz sekciju Discussions također dostupnu na GitHubu vašeg projekta. -->

# Naziv projekta
<h2>STONKS - Super tehnologija optimalno naprednih kasa Stonks</h2>

👉
<a href="https://drive.google.com/file/d/13aoFGcPRaKiJIIHuqjvnR9d5AhfHIhH9/view?usp=share_link">Link za instalaciju softvera</a>👈

Projekt je rađen u tročlanom timu prema tablicama u nastavku, u Windows Forms tehnologiji i Entity Frameworku.


<p align="center">
<img src="https://i.ytimg.com/vi/if-2M3K1tqk/maxresdefault.jpg" height="400px" width="600px"  > </img>
</p>



Projekt se bavi temom uobičajene blagajne kojom se koriste sve današnje trgovine uz nekoliko dodatnih, nesvakidašnjih mogućnosti (npr. face recognition pri prijavi).

Postoje 2 vrste prijavljenih korisnika, zaposlenika trgovine - obični zaposlenik i voditelj trgovine (koji ima mogućnost dodavanja artikala i unosa primke, a te su mogućnosti onemogućene običnome zaposleniku).

Zaposlenici mogu skenirati barkodove artikala ili ih ručno odabirati te se ti artikli dodaju na račun prilikom kupnje. Zaposlenik bira način plaćanja kupca te se dodatne informacije (datum, ime prodavača) automatski zapisuju na račun koji će se moći prikazati u PDF obliku. Ukoliko dođe do neočekivane promjene, zaposlenik može stornirati račun te se stanje artikala u trgovini vraća na ono kao da se kupnja nije nikad ni dogodila.
Naravno, mogu se unijeti novi artikli te se povećati stanje proizvoda na skladištu ukoliko dođe nova primka osiguravajući da će u aplikaciji biti ažurni i točni podaci.

Zaposlenici vide sve artikle i sve račune pa, pošto će ih biti puno, imaju neke opcije naprednog pretraživanja, sortiranja i filtriranja. Na kraju svakog dana moći će se izraditi dnevni izvještaj o prometu kako bi uprava trgovine mogla pratiti glavne podatke o poslovanju trgovine.

Svu dokumentaciju o softveru moguće je pronaći na Wiki dijelu repozitorija. Dijagrami su izrađeni pomoću Visual Paradigma.



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



#1. O projektu
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


#2. Specifikacija korisničkih softverskih zahtjeva

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





