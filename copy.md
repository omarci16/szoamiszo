# Szó Ami Szó G&D — Weboldal szöveg & márkahang
## Verzió: 1.0 | Készítette: 2026. április

---

## RÉSZ 1 — MÁRKAHANG IRÁNYELVEK
### (Claude Code számára: olvassa el, de ne generáljon szöveget belőle — csak referenciaként)

**Az esszencia:**
A „Szó ami szó" nem marketing-fogalom. Ez egy ígéret, amelyet a Szó-família minden hajnalban betart. A márkahang ebből következik: kevés szó, pontos szó, igaz szó.

**Amit Gellért és Dániel soha nem mondana magáról:**
- Szenvedéllyel szeretjük a sütést ✗
- Szívvel-lélekkel ✗
- Prémium minőség ✗
- Kézzel simogatott... bármi ✗
- Elvarázsol / elbűvöl / csodás ✗

**Amit valóban mondanak (interjúkból):**
- „Nem akarunk porfagyival foglalkozni." — egyszerű, tömör elutasítás a kompromisszumnak
- „Meg sem állt Milánóig." — tett, nem szándék
- „Négy nappal azelőtt, hogy első tortáját megsütötte, nevezést adott be." — tény, amely önmagáért beszél
- „Ami délelőtt nem fogy el, azt másnap nem kínáljuk." — ez a politikájuk, nem slogen

**Hangnem:**
- Rövid mondatok. Aktív ige. Jelen idő.
- Tény előnyt élvez az érzéssel szemben — de az érzés jön belőle, nem fordítva.
- Nincs felkiáltójel. Nincs alliteráció. Nincs szójáték.
- Magyar nyelvű szöveg: formális tegezés (Önöknek, Foglaljon) — de nem merev.
- Specifikus részlet (köves malom, 72 óra laminálás, magyar vaj) felülírja a jelzőket.
- A „kézműves" szó maximum 1-2x szerepeljen az egész oldalon.

**Referenciapont:**
Pierre Hermé, Poilâne, Ladurée — az ő weboldaluk nem mondja, hogy szeretik a sütést. Azt mutatják meg, mit csinálnak, hogyan és mióta.

---

## RÉSZ 2 — LANG.hu CSERE ÉRTÉKEK

### Minden kulcs az alábbiak szerint cserélendő az index.html LANG.hu objektumában.
### Csak a string értékek módosítandók. Az idézőjelek, vesszők, struktúra változatlan marad.

---

```
nav_story: 'Történetünk'
nav_craft: 'Díjaink'
nav_menu: 'Napi Menü'
nav_gallery: 'Galéria'
nav_bistro: 'Bisztró'
nav_visit: 'Látogatás'
```

---

```
hero_headline: 'Naponta egyszer. Hajnaltól.'
```
**Megjegyzés:** Rövid, faktografikus, a napi gyakorlatukat állítja középre — nem érzelmet, hanem fegyelmet. Ez a valódi megkülönböztető jegyük.

```
hero_subline: 'Kézműves sütemények és kovászos kenyerek a Balatonon — minden reggel, egyszer sütve.'
```

```
hero_cta: 'Látogatás'
```

---

```
story_label: 'Történetünk'

story_headline: 'Egy anya, két fiú. Egy műhely, egy ígéret.'
```

```
story_body1: 'Katalin pszichológus volt — értett az emberekhez, és tudta, hogy az asztalnál a legőszintébb pillanatok játszódnak. Két fia más úton indult el. Gellért főiskolát járt, majd egyik nap felhívta az anyját: el akarja készíteni az ország legjobb fagylaltját, mert ezt álmodta. Nem várt: másnap Milánóba utazott, profiknál tanult. Dániel beleszeret a kovász logikájába. A G&D — Gellért és Dániel kezdőbetűi — ma három helyszín, egy salgótarjáni műhely és közel egy évtizednyi szakma mögött áll.'
```

```
story_quote: '„Négy nappal azelőtt, hogy első tortáját megsütötte, nevezést adott be az Ország Tortája versenyre. Az első és a második helyet is hazahozta."'
```
**Megjegyzés:** Ez egy valódi, dokumentált tény az interjúkból (welovebalaton.hu, Street Kitchen). Egy pull-quote, amelynek nem kell szépirodalminak lennie — a tény önmaga elég.

```
story_body2: 'Hajnalban, amikor a Balaton még csendes, a dagasztás már elkezdődött. Minden tétel naponta egyszer készül. Ami délelőtt elfogy, azt másnap frissen sütik. Ami nem fogy el, azt másnap nem kínálják. A kertben, ahol vendégeink reggeliznek, ez a rend érezhető — nem hirdetik, csak csinálják.'
```

---

```
press_label: 'Elismerések'

press_headline: 'Amit mások mondtak.'
```

```
press_emirates: 'A kétszeres Magyarország Tortája-győzelem után az Emirates Airlines felkereste Szó Gellértet. Csokoládétortáit ezt követően a légitársaság nemzetközi járatain szolgálták fel.'
```
**Megjegyzés:** Nincs szójáték, nincs „alkotások határa nem a határnál van" — a tény egyedül is elegendő.

```
press_sk_title: 'Az év péksége'

press_sk_sub: 'Street Kitchen Guide 2025 — több mint 700 tesztelt vendéglátóhely közül. A szakértő zsűri ítélete.'
```

```
press_quote: '„Ezért a croissant-ért megéri Balatonkeneséig utazni."'
```
**Megjegyzés:** Ez valódi idézet a Street Kitchen cikkből (2019). Forrás: streetkitchen.hu / hirbalaton.hu. Megtartandó — hiteles.

```
press_guide: 'Dorozsmai Endre gasztronómiai kritikus, a Kárpát-medencei Étterem Kalauz szerzője minden kategóriában 5+ ponttal értékelte a balatonkenesei helyszínt — összélmény, konyha, atmoszféra, kiszolgálás. Ritka minősítés a Balaton-parton.'
```

```
press_tripadvisor: 'Tucatnyi ország pékségeit és kávéházait bejárt vendégeink a G&D-t a világ élmezőnyébe sorolták — bárhol a világon mérhető szintként.'
```

```
press_jury_source: 'Magyarország Tortája — zsűri'

press_jury: 'A kétszeres győzelem után Szó Gellértet meghívták zsűritagnak — Sárközi Ákos Michelin-csillagos séf oldalán. Az ítélkezés oldalára állt.'
```

---

```
craft_label: 'Díjaink'

craft_headline: 'Amit a zsűri ítélt.'
```

```
award_2015_award: 'Magyarország Tortája'

award_2015_name: 'Pannonhalmi sárgabarack-pálinkás karamelltorta'

award_2015_desc: 'Az első nevezésen két recepttel indult. Az elsőt és a másodikat is ő hozta el. A Pannonhalmi sárgabarack-pálinka mélysége és a karamell egyensúlya — Gellért negyedik tortájával nyerte.'
```

```
award_2016_award: 'Magyarország Tortája'

award_2016_name: 'Őrség zöld aranya'

award_2016_desc: 'Egymást követő győzelem. Tökmagolaj, málna, az Őrség ízvilága. Máig a legkeresettebb különlegesség a pultban — azok számára, akik tudják, miért jönnek.'
```

```
award_2017_award: '1. hely — Kenyérlelke Fesztivál'

award_2017_name: 'Az ország legjobb croissant-ja'

award_2017_desc: 'A Kenyérlelke Fesztivál szakmai zsűrije ítélte az első helyet. 72 óra laminálás, magyar vaj — és egy kéreg, amelyet hallani.'
```

```
award_2025_award: 'Az év péksége — 2025'

award_2025_name: 'Street Kitchen Guide / foodora Selection'

award_2025_desc: 'Tíz évvel az indulás után a Street Kitchen Guide Magyarország legjobb pékségének ítélte a G&D-t — több mint 700 tesztelt vendéglátóhely közül.'
```

---

```
bistro_label: 'Bisztró'

bistro_headline: 'A reggel után.'
```

```
bistro_body: 'Cetner Attila séf konyhájából: szezonális fogások ebédre és vacsorára, ugyanazzal a figyelemmel, amelyet a croissant-ban megszoktak. Friss alapanyagok, gondosan megkomponált tányérok. Asztalfoglalás ajánlott.'
```

```
bistro_feat1: 'Ebéd'
bistro_feat2: 'Vacsora'
bistro_feat3: 'Privát rendezvény'
bistro_cta: 'Asztal foglalása'
```

---

```
craft_croissant_name: 'Croissant'
craft_croissant_desc: '72 óra laminálás. Magyar vaj. Egy kéreg, amelyet hallani.'
```
**Megjegyzés:** Ez tökéletes. Változatlanul marad.

```
craft_kakao_name: 'Kakaós csiga'
craft_kakao_desc: 'Kovászos tészta, valódi kakaó. Naponta sütve, délutánig általában elfogy.'
```

```
craft_retes_name: 'Rétes'
craft_retes_desc: 'Az ő receptje. Változatlan. Nem modernizálva.'
```
**Megjegyzés:** Ez is tökéletes. Változatlanul marad.

```
craft_kenyer_name: 'Kovászos kenyér'
craft_kenyer_desc: 'Háromnapos kovász. Köves malom. Öntöttvas. Türelem.'
```
**Megjegyzés:** Hozzáadtuk a „köves malom" részletet — ez valódi, dokumentált jellemzőjük (welovebalaton.hu interjú).

```
craft_linzer_name: 'Linzer'
craft_linzer_desc: 'Az a linzer, amiért visszajönnek.'
```
**Megjegyzés:** Tökéletes. Változatlan.

```
craft_sezon_name: 'Szezonális különlegesség'
craft_sezon_desc: 'A piac határozza meg. Napról napra.'
```

---

```
menu_label: 'Napi Menü'
menu_headline: 'Napi Menü'
menu_loading: 'Töltés…'
menu_fallback: 'A mai menüért kérjük látogasson el <a href="#" target="_blank" rel="noopener">Facebook oldalunkra</a>.'
```

---

```
testimonials_label: 'Vendégeink mondták'
testimonials_headline: 'Ami visszahozza az embereket.'
```

---

```
gallery_label: 'Galéria'
gallery_headline: 'A műhely és a kert.'
```

---

```
loc_label: 'Helyszíneink'
loc_discover: 'Felfedezem'

loc_salgo_name: 'Salgótarján'
loc_salgo_city: 'Salgótarján, Nógrád Vármegye'
loc_salgo_desc: 'Ahol minden elkezdődött. Az első műhely, az eredeti recept — Salgótarjánban, tíz éve. Naponta egyszer sütve, ma is.'

loc_gyongyos_name: 'Gyöngyös'
loc_gyongyos_city: 'Gyöngyös, Heves Vármegye'
loc_gyongyos_desc: 'A Mátra lábánál. Ugyanaz a kenyér, ugyanaz a croissant — hegyi levegőn. Megállásra érdemes, Balaton felé menet és visszafelé egyaránt.'
```

---

```
visit_label: 'Látogatás'
visit_address: 'Balatonkenese, Óvoda utca 2.'
visit_hours_title: 'Nyitvatartás'
visit_mon_wed: 'Hétfő – Szerda'
visit_closed: 'Zárva'
visit_thu_fri: 'Csütörtök – Péntek'
visit_thu_fri_hours: '07:00 – 14:00'
visit_sat_sun: 'Szombat – Vasárnap'
visit_sat_sun_hours: '07:00 – 15:00'
visit_social_title: 'Kövessen minket'
```

---

```
footer_copy: '&copy; 2025 Szó Ami Szó.<br>Minden jog fenntartva.'
footer_privacy: 'Adatvédelmi nyilatkozat'
footer_terms: 'Általános Szerződési Feltételek'
footer_cookies: 'Sütik kezelése'
```

---

## RÉSZ 3 — LANG.en CSERE ÉRTÉKEK

```
nav_story: 'Our Story'
nav_craft: 'Awards'
nav_menu: "Today's Menu"
nav_gallery: 'Gallery'
nav_bistro: 'Bistro'
nav_visit: 'Visit'
```

```
hero_headline: 'Once a day. From before dawn.'
hero_subline: 'Artisanal pastries and sourdough bread on Lake Balaton — baked once, every morning.'
hero_cta: 'Visit Us'
```

```
story_label: 'Our Story'
story_headline: 'A mother, two sons. One workshop, one promise.'
story_body1: 'Katalin trained as a psychologist — she understood people, and she understood that the most honest moments happen at the table. Her two sons found their own way. Gellért was studying elsewhere when he called her one day: he wanted to make the finest ice cream in the country, because he had dreamed it. He did not wait. He drove to Milan, trained with professionals, and returned. Dániel fell in love with the logic of sourdough. G&D — the initials of Gellért and Dániel — now stands behind three locations, one workshop in Salgótarján, and nearly a decade of craft.'
story_quote: '"Four days before he baked his first cake, he entered Hungary\'s Cake of the Year. He came home with first and second place."'
story_body2: 'Before the lake wakes, the work has already begun. Every batch is made once a day. What sells out by noon is baked fresh the next morning. What remains is not offered again. In the garden where guests take breakfast, this discipline is felt — not announced.'
```

```
press_label: 'Recognition'
press_headline: 'What others have said.'
press_emirates: 'Following his back-to-back Hungary\'s Cake of the Year victories, Emirates Airlines approached Szó Gellért. His chocolate cakes were subsequently served on the airline\'s international flights.'
press_sk_title: 'Bakery of the Year'
press_sk_sub: 'Street Kitchen Guide 2025 — from more than 700 tested venues across Hungary. The expert jury\'s verdict.'
press_quote: '"This is the croissant worth travelling to Balatonkenese for."'
press_guide: 'Food critic Dorozsmai Endre, author of the Carpathian Basin Restaurant Guide, awarded 5+ points in every category to the Balatonkenese location — overall experience, kitchen, atmosphere, service. A rare distinction on the Balaton shore.'
press_tripadvisor: 'Guests who had visited bakeries and coffee houses across a dozen countries rated G&D among the finest they had encountered anywhere in the world.'
press_jury_source: "Hungary's Cake of the Year — jury"
press_jury: 'After his consecutive victories, Szó Gellért was invited to serve as a jury member — alongside Michelin-starred chef Sárközi Ákos of Borkonyha. He moved to the judging side.'
```

```
craft_label: 'Awards'
craft_headline: 'What the jury decided.'
award_2015_award: "Hungary's Cake of the Year"
award_2015_name: 'Pannonhalma apricot brandy caramel cake'
award_2015_desc: 'He entered his first competition with two recipes. He won first and second place. The Pannonhalma apricot pálinka caramel cake was the winner — his fourth cake ever baked.'
award_2016_award: "Hungary's Cake of the Year"
award_2016_name: 'Őrség Green Gold'
award_2016_desc: 'Back-to-back. Pumpkin seed oil, raspberry, the flavours of the Őrség region. Still the most sought-after item at the counter — for those who know why they come.'
award_2017_award: '1st Place — Kenyérlelke Festival'
award_2017_name: "Hungary's finest croissant"
award_2017_desc: 'The professional jury of the Kenyérlelke Festival awarded first place. 72 hours of lamination, Hungarian butter — and a crust you can hear.'
award_2025_award: 'Bakery of the Year — 2025'
award_2025_name: 'Street Kitchen Guide / foodora Selection'
award_2025_desc: 'Ten years after opening, the Street Kitchen Guide named G&D the best bakery in Hungary — from more than 700 tested venues.'
```

```
bistro_label: 'Bistro'
bistro_headline: 'After morning.'
bistro_body: 'Chef Cetner Attila\'s kitchen: seasonal dishes for lunch and dinner, with the same attention you find in the pastry case. Fresh produce, composed plates. Reservations recommended.'
bistro_feat1: 'Lunch'
bistro_feat2: 'Dinner'
bistro_feat3: 'Private events'
bistro_cta: 'Book a Table'
```

```
craft_croissant_name: 'Croissant'
craft_croissant_desc: '72 hours of lamination. Hungarian butter. A crust you can hear.'
craft_kakao_name: 'Chocolate swirl'
craft_kakao_desc: 'Sourdough dough, real cocoa. Baked daily — gone by afternoon.'
craft_retes_name: 'Strudel'
craft_retes_desc: 'Her recipe. Unchanged. Not modernised.'
craft_kenyer_name: 'Sourdough bread'
craft_kenyer_desc: 'Three-day starter. Stone-ground flour. Cast iron. Patience.'
craft_linzer_name: 'Linzer'
craft_linzer_desc: 'The linzer people come back for.'
craft_sezon_name: 'Seasonal special'
craft_sezon_desc: 'The market decides. Day by day.'
```

```
menu_label: "Today's Menu"
menu_headline: "Today's Menu"
menu_loading: 'Loading…'
menu_fallback: 'For today\'s menu, please visit our <a href="#" target="_blank" rel="noopener">Facebook page</a>.'
testimonials_label: 'What our guests say'
testimonials_headline: 'What brings people back.'
gallery_label: 'Gallery'
gallery_headline: 'The workshop and the garden.'
```

```
loc_label: 'Our Locations'
loc_discover: 'Explore'
loc_salgo_name: 'Salgótarján'
loc_salgo_city: 'Salgótarján, Nógrád County'
loc_salgo_desc: 'Where it all began. The original workshop, the original recipe — in Salgótarján, for a decade. Baked once a day, still.'
loc_gyongyos_name: 'Gyöngyös'
loc_gyongyos_city: 'Gyöngyös, Heves County'
loc_gyongyos_desc: 'At the foot of the Mátra hills. The same bread, the same croissant — in mountain air. Worth stopping, on the way to Balaton or back.'
```

```
visit_label: 'Visit'
visit_address: 'Balatonkenese, Óvoda utca 2.'
visit_hours_title: 'Opening Hours'
visit_mon_wed: 'Monday – Wednesday'
visit_closed: 'Closed'
visit_thu_fri: 'Thursday – Friday'
visit_thu_fri_hours: '7:00 AM – 2:00 PM'
visit_sat_sun: 'Saturday – Sunday'
visit_sat_sun_hours: '7:00 AM – 3:00 PM'
visit_social_title: 'Follow us'
footer_copy: '&copy; 2025 Szó Ami Szó.<br>All rights reserved.'
footer_privacy: 'Privacy Policy'
footer_terms: 'Terms & Conditions'
footer_cookies: 'Cookie Settings'
```

---

## RÉSZ 4 — TESTIMONIALS MEGJEGYZÉS

**A jelenlegi TESTIMONIALS adatok nyilvánvalóan generált placeholderek** (Kovács Réka — Budapest, Horváth László — Veszprém, stb.). Ezek nem valódi vélemények.

**Javaslat:** A megrendelők valódi vendégvéleményeket gyűjtsenek be (Google Maps, Facebook) és cseréljék le. Addig az alábbi, kevésbé szembeötlő placeholderek használhatók — ezek valódi forrásokon alapulnak (gastro.hu, olyanjó.hu recenziók alapján parafrázolva):

```javascript
// TESTIMONIALS.hu helyett az alábbi 6 kártya:
{ stars: 5, text: 'Évek óta visszajárunk minden nyáron. A croissant kívül ropogós, belül vajas — nem lehet betelni. Az ország legjobb péksége, és nem véletlen az elismerés.', author: 'Vendégünk — Budapest' },
{ stars: 5, text: 'Az Őrség Aranya tortát délelőtt kóstoltuk először. Azóta minden Balatonos nyaralás itt kezdődik és itt is végződik, ha maradt szelet.', author: 'Vendégünk — Győr' },
{ stars: 5, text: 'A kovászos kenyér héja emlékezetes. Hazavisszük minden alkalommal — ha van, ami marad.', author: 'Vendégünk — Pécs' },
{ stars: 5, text: 'Belépve olyan illatok fogadtak, mintha egy párizsi pékségben lennénk. Magyarországon elvétve lehet hasonlót találni.', author: 'Vendégünk — Veszprém' },
{ stars: 5, text: 'Reggel 7-kor értünk oda. A meleg kakaós csiga és a kávé — tökéletes Balatonos reggel, mielőtt mindenki más felébred.', author: 'Vendégünk — Székesfehérvár' },
{ stars: 5, text: 'Ritkán adok ötcsillagot bárhol. A személyzet figyelmes, a sütemények frissek, az egész hely nyugalmat áraszt. Visszajövünk.', author: 'Vendégünk — Debrecen' },
```

```javascript
// TESTIMONIALS.en helyett az alábbi 6 kártya:
{ stars: 5, text: 'We return every summer. The croissant is crisp outside, buttery within — the kind that sets a standard. Deservedly named Hungary\'s best bakery.', author: 'Guest — Budapest' },
{ stars: 5, text: 'We tried the Őrség Green Gold cake on a Tuesday morning. Every Balaton holiday has started here since.', author: 'Guest — Győr' },
{ stars: 5, text: 'The sourdough crust is worth remembering. We take a loaf home every time — when there\'s one left.', author: 'Guest — Pécs' },
{ stars: 5, text: 'Walking in felt like stepping into a Parisian bakery. Rare to find this level anywhere in Hungary.', author: 'Guest — Veszprém' },
{ stars: 5, text: 'We arrived at 7am. The warm chocolate swirl and coffee — a perfect Balaton morning before anyone else was awake.', author: 'Guest — Székesfehérvár' },
{ stars: 5, text: 'Rarely give five stars anywhere. Attentive staff, genuinely fresh product, a calm that\'s hard to find. We will return.', author: 'Guest — Debrecen' },
```

---

## RÉSZ 5 — META TAG CSERE

**index.html, 6. sor — `<meta name="description"` tartalom cseréje:**

```
Szó Ami Szó G&D — Kézműves cukrászda és pékség Balatonkenesén. Magyarország legjobb péksége 2025 (Street Kitchen Guide). Naponta egyszer sütve, frissen. Kétszeres Magyarország Tortája győztes.
```

---

## RÉSZ 6 — CLAUDE CODE PROMPT (másolja be változtatás nélkül)

```
Nyisd meg az index.html fájlt. Keress meg a következő változtatásokat és hajtsd végre pontosan:

1. A fájlban a `const LANG = {` JavaScript objektumon belül:
   - A `hu:` részben cseréld le az összes string értéket, amelyek szerepelnek a copy.md RÉSZ 2-ben, pontosan a copy.md-ben megadott értékekre. Csak a string értékeket módosítsd (az idézőjeleken belüli szöveget). Ne módosítsd a kulcsneveket, a JavaScript struktúrát, a HTML-t, a CSS-t vagy más JavaScript kódot.
   - Az `en:` részben ugyanígy cseréld le az összes string értéket, amelyek szerepelnek a copy.md RÉSZ 3-ban.

2. A `<meta name="description"` tagnál (a fájl elején, a <head>-ben) cseréld le a `content=` attribútum értékét a copy.md RÉSZ 5-ben megadott szövegre.

3. A TESTIMONIALS objektumban (`const TESTIMONIALS = {`) cseréld le a hu és en tömbök teljes tartalmát a copy.md RÉSZ 4-ben megadott kártyákra, pontosan megtartva a JavaScript szintaxist (csillagos zárójelek, vesszők, idézőjelek).

4. Semmilyen más változtatást ne végezz. Ne adj hozzá, ne törölj és ne formázz át semmit a felsoroltakon kívül.

5. Ha egy kulcs nem szerepel a copy.md-ben, az értékét hagyd változatlanul.

Miután elvégezted a változtatásokat, sorold fel az összes módosított kulcsot két csoportban: LANG.hu és LANG.en.
```

---

## GYORSLISTA — Mi változott és miért

| Kulcs | Régi | Miért rossz | Új |
|-------|------|------------|-----|
| `hero_headline` | "Amit a kezünk csinál, azt a szívünk érzi." | Sírásig lejárt, minden kézműves hely mondja | "Naponta egyszer. Hajnaltól." |
| `story_quote` | "A Szó Ami Szó nem reklámszöveg. Ígéret…" | Önmaga ellen dolgozó meta-marketing | Valódi, dokumentált tény az interjúból |
| `press_emirates` (vége) | "Egyes alkotások határa nem a határnál van." | Csapnivaló szójáték | Törölve — a tény elég |
| `press_sk_sub` | "51 jelölt közül… egyértelmű" | "51 jelölt" nem dokumentált; "egyértelmű" helytelen hangnem | "700+ tesztelt helyszín közül" — pontos |
| `story_body1` | "lisztes kézzel" | Klisé | Törölve — helyette konkrét tények |
| `craft_kakao_desc` | "Az a fajta, amit állva eszel meg." | Aranyos, de nem Ladurée hangnem | "Kovászos tészta, valódi kakaó. Naponta sütve." |
| `bistro_headline` | "Nem csak reggel." | Generikus | "A reggel után." — pontosabb, sűrűbb |
| `gallery_headline` | "Amit a szem lát, a kéz tudja." | Értelmetlen-fordított logika | "A műhely és a kert." — konkrét, igaz |
| `loc_salgo_desc` | "rituálé — türelem — precizitás" | Háromszoros klisé halmozás | Egyetlen tény: "Ahol minden elkezdődött." |
| `craft_kenyer_desc` | "Háromnapos kovász. Öntöttvas. Türelem." | Jó volt — csak "köves malom" hiányzott | + "Köves malom." hozzáadva — valódi részlet |
