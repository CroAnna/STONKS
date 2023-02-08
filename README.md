
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

