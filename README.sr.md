<a href="https://www.ballet-dobrilanovkov.com/"><img src="media/cover.jpg" alt="La Sylphide, naslovna strana na laptopu i telefonu" width="100%"></a>

# La Sylphide

Sajt baletske škole iz Novog Sada, osnovane 1991, na srpskom, engleskom i ruskom, prepisan sa WordPress-a iz 2016. u običan PHP.

**[ballet-dobrilanovkov.com](https://www.ballet-dobrilanovkov.com/)** · [Studija slučaja](https://svilenkovic.rs/radovi/la-sylphide) · [English](README.md)

> [!NOTE]
> Klijentski projekat. Izvorni kod pripada klijentu i čuva se u privatnom repozitorijumu. Ova stranica opisuje šta sam uradio i kako.

<table>
  <tr><td><b>Klijent</b></td><td>Baletska škola Dobrile Novkov La Sylphide</td></tr>
  <tr><td><b>Delatnost</b></td><td>Klasičan balet za decu i odrasle po metodi Vaganove</td></tr>
  <tr><td><b>Lokacija</b></td><td>Novi Sad</td></tr>
  <tr><td><b>Vrsta</b></td><td>Sajt sa više strana na tri jezika</td></tr>
  <tr><td><b>Moj deo posla</b></td><td>Redizajn, izrada, selidba, SEO i održavanje</td></tr>
  <tr><td><b>Tehnologije</b></td><td>PHP, no CMS, hreflang sr/en/ru, WebP, View Transitions</td></tr>
</table>

## O projektu

La Sylphide radi u Novom Sadu od 1991. Program je klasičan balet po nastavnom planu Akademije Vaganove, sa grupama za decu od tri godine naviše i tri grupe za odrasle. Stari sajt je bio WordPress 4.6 iz 2016. sa napuštenom temom: sedam strana, prazni plejeri na mestu četiri od pet snimaka koji su odavno skinuti sa YouTube-a i nijedna strana o baletu za odrasle.

Prvo smo se dogovorili za osvežavanje, ali sam posle pregleda koda predložio pisanje od nule i škola je pristala. Nov sajt čine obične PHP strane sa zajedničkim delovima kroz include, bez baze i bez administracije, jer se sadržaj menja jednom ili dvaput godišnje. Prijava za upis radi i bez JavaScript-a: CSRF token se pravi na serveru, forma se šalje običnim POST-om i strana se vraća sa porukom, pa prijava prolazi i sa starijeg telefona i preko slabe veze.

## Šta sam uradio

- Srpske strane uz englesku i rusku ulaznu stranu, povezane hreflang oznakama za sr-Latn, en i ru, sa x-default koji vodi na srpsku verziju
- Fontovi na istom serveru, podeljeni na latinicu, proširenu latinicu i ćirilicu, da ruska strana ima svoja slova, a srpska ih ne preuzima
- Snimci i mapa se učitavaju tek kad ih posetilac zatraži, YouTube preko domena bez kolačića, a prelaz između strana ide kroz View Transitions, uz učitavanje unapred kad miš pređe preko linka
- Kod koji radi i na PHP-u 7.4 i na 8.3, sa jednom konfiguracijom koja prepoznaje host i bira osnovnu adresu, primaoca prijava i da li strane smeju da se indeksiraju
- Selidba tek posle pune rezervne kopije: stari WordPress sklonjen van dohvata za svaki slučaj, stare adrese slika sačuvane, preusmerenja u jednom skoku i odgovor 410 za zaostale WordPress adrese
- Svetla i tamna tema primenjena pre prvog iscrtavanja, sa dve odvojene bordo vrednosti u tamnoj temi da tekst zadrži kontrast

## Merenja

| | Performanse | Pristupačnost | Dobre prakse | SEO |
| :-- | :-: | :-: | :-: | :-: |
| Telefon | 97 | 100 | 100 | 100 |
| Desktop | 100 | 100 | 100 | 100 |

PageSpeed Insights, laboratorijsko merenje živog sajta, septembar 2026. Sigurnosna zaglavlja: 6 od 6. axe provera pristupačnosti: bez prekršaja. Strukturisani podaci: `EducationalOrganization`, `LocalBusiness`.

## Snimci ekrana

<table>
  <tr>
    <td width="68%" valign="top"><img src="media/desktop.webp" alt="La Sylphide, naslovna strana na ekranu širine 1440 px"></td>
    <td width="32%" valign="top"><img src="media/mobile.webp" alt="La Sylphide, naslovna strana na telefonu"></td>
  </tr>
</table>

<img src="media/inner-1.webp" alt="Časovi klasičnog baleta za svaki uzrast, razdvojeni po programu">
<sub>Časovi klasičnog baleta za svaki uzrast, razdvojeni po programu</sub>

<img src="media/inner-2.webp" alt="Sala škole i deo o programu Akademije Vaganove">
<sub>Sala škole i deo o programu Akademije Vaganove</sub>

---

<sub>Izrada: [D. Svilenković](https://svilenkovic.rs).</sub>
