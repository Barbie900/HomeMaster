# HomeMaster 🏠🔨

**Plugin za Claude Code, ki načrtuje celovito prenovo doma v lastni režiji, prostor za prostorom, s povezanim znanjem.**

🇬🇧 [English → README.md](README.md)

Večina nasvetov za prenovo je razdrobljena. Navodila za ploščice ne vedo, da si estrih vlila prejšnji teden, navodila za vodovod pa ne vedo, kje bo končni tlak. HomeMaster ta področja poveže. Preden napiše navodila za neko delo, preveri **graf odvisnosti** in **tvoj dnevnik projekta** ter te opozori na vse, kar vpliva z drugih področij.

> Primer: vprašaš za navodila za polaganje talnih ploščic. HomeMaster v dnevniku vidi, da je bil estrih vlit pred 12 dnevi na talno ogrevanje, in te **ustavi**. Estrih najprej potrebuje CM-meritev vlage (≤ 1,8 CM-% za ogrevan cementni estrih) in protokol ogrevanja. Šele nato dobiš celotna navodila z natančnim orodjem, materialom, količinami, triki in kontrolami med delom.

## Kaj dobiš

| | |
|---|---|
| 🧭 **Nastavitev projekta** | Intervju o tvojem domu (hiša / stanovanje / vikend, letnik, način gradnje, proračun, znanje, orodje, ki ga že imaš) |
| 🔗 **Graf odvisnosti** | Vsako delo ve, kaj mora biti narejeno prej, kaj blokira in kaj gre lahko narobe med področji |
| 📋 **Navodila za delo** | Pogoji, orodje (imaš / kupi / izposodi), material s količinami in odpadom, koraki, triki, pogoste napake, časi sušenja, kontrola kakovosti |
| ⚖️ **Priporočila** | Primerja možnosti (npr. tekoča hidroizolacija ali trakovi) in pove, kaj je boljše *za tvoj primer* |
| 🦺 **Varnostni pregled** | Opozori na dela, ki zakonsko ali praktično zahtevajo strokovnjaka (plin, meritve in atest elektroinštalacij, nosilne stene, azbest) |
| 🗒️ **Spomin projekta** | Dnevnik, kaj je narejeno in kdaj, da kasnejši nasveti gradijo na tem |

## Kako delaš z njim: majhni koraki, po vrstnem redu

Navodila za cel prostor bi bila predolga. HomeMaster razdeli vsak prostor na **delovne pakete** in drži vrstni red:

1. `/homemaster:plan-room`: urejen seznam za tvoj prostor (pri kopalnici: odtoki, WC element, odtok za tuš, dovodne cevi, topla voda, preizkusi, estrih, hidroizolacija, ploščice, WC školjka, umivalnik, tuš, steklo ...), s čakalnimi časi, kdo kaj dela in kaj naročiti najprej.
2. `/homemaster:next-step`: **po en paket naenkrat** kot kratka delovna kartica (orodje, material, koraki, kontrole), po preverjanju, da je vse pred njim narejeno.
3. Povej, ko je korak končan. Posodobi načrt in dnevnik ter odpre naslednjega.

## Namestitev

V Claude Code:

```
/plugin marketplace add Barbie900/HomeMaster
/plugin install homemaster@homemaster
```

Nato ustvari **ločeno mapo za svoj dom** (nikoli znotraj plugina), v njej odpri Claude Code in zaženi:

```
/homemaster:new-project
```

## Kje ga lahko uporabljaš

HomeMaster je plugin za Claude Code, zato deluje povsod, kjer deluje Claude Code, ne samo v terminalu:

| Kje | Kako |
|---|---|
| **Claude namizna aplikacija, zavihek Code** (navaden klepet) | Začni sejo v **mapi svojega doma** in vpiši `/homemaster:new-project`. |
| **Razširitev za VS Code / JetBrains** | Odpri mapo svojega doma, odpri Claude in vpiši `/homemaster:new-project`. |
| **Terminal** | `cd` v mapo svojega doma, zaženi `claude` in vpiši `/homemaster:new-project`. |

Plugin namestiš enkrat (glej zgoraj). Potem se lahko z njim pogovarjaš kar v navadnem jeziku (»želim prenoviti kopalnico«, »kaj je naslednji korak?«). Poševni ukazi so samo bližnjice.

> **claude.ai v spletnem brskalniku** plugine za Claude Code ne nalaga. Različica za spletni klepet (skilli ali Project) je v [ROADMAP.md](ROADMAP.md).

## Jezik

Struktura in baza znanja sta v angleščini, da lahko prispeva kdorkoli. **Agenti odgovarjajo v jeziku, nastavljenem v profilu projekta.** Slovenščina ima vgrajen slovar strokovnih izrazov in regionalne opombe.

## Stanje

Zgodnji razvoj. HomeMaster načrtuje **celoten dom**, za vsak tip prostora ima svoj vodič:

| Tip prostora | Pokrito |
|---|---|
| Kopalnica in WC | najpodrobneje (hidroizolacija, estrih, ploščice, električne cone) |
| Kuhinja | postavitev, priključki, odsesavanje, montaža |
| Dnevna soba, spalnica, hodnik | tla, slikanje, ogrevanje, akustika, varnost |
| Klet | diagnostika vlage, hidroizolacija, radon, preureditev |
| Zunanje stopnice, terasa | geometrija, zmrzal, odvodnjavanje, ploščice, tlakovanje, lesena terasa, ograje |
| Wellness | savna, parna kopel, masažni bazen (načrtovanje in pravila gradnje) |
| Streha in podstrešje | pregled, varno delo, manjša popravila, preureditev podstrešja |
| Fasada | fasadni sistem (kontaktna fasada), omet, popravila, oder in dovoljenja |
| Vrtne zgradbe | uta, pergola, nadstrešek, ograja, oporni zid, temelji |
| Bazen | načrtovanje, konstrukcija, filtracija, varnost, kemija (elektrika vedno pooblaščeni) |
| Notranje stopnice | kontrolni pregled, popravilo, obnova, zamenjava, vpliv višin tal |
| Zunanji bazen | izbira lokacije, ogrevanje in prekrivalo, naravni bazen, zimska zaščita |
| Dimnik, peč, kamin | pregled, dimovod, podnožje, zrak za zgorevanje, varna uporaba (dimnikar odobri) |
| Vrtna ureditev | pregled, zemlja, trata, grede, drevesa, žive meje, vrstni red del |
| Namakanje | pretok in tlak, cone, kapljično in razpršilci, protipovratni ventil, zazimitev |
| Pametni dom | kabliranje med grobimi deli, standardi, lokalno upravljanje, varnost in zasebnost |
| Drugo (pisarna, pralnica, garaža) | preslikano na najbližji tip |

Poleg tega **načrtovanje celotne hiše**: vrstni red faz in prostorov, skupne odločitve (razdelilna omara, ogrevanje, izolacija, okna), bivanje med deli, proračun in dobavni roki.

Vse je **prvi osnutek** in ga morajo pregledati mojstri ter preizkusiti pravi projekt. Glej [ROADMAP.md](ROADMAP.md).

## ⚠️ Omejitev odgovornosti

HomeMaster daje smernice, ne jamstva. Vedno upoštevaj tehnične liste proizvajalcev, gradbene predpise in lokalno zakonodajo. Za plin, priklop na omrežje, meritve in atest električnih inštalacij ter posege v nosilno konstrukcijo so v večini držav potrebni pooblaščeni strokovnjaki. Za svojo varnost si odgovoren sam.

## Licenca

MIT
