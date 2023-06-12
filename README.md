# Local Tuya Tutorial SK

## Ako integrovať Tuya zariadenia do Home Assistanta cez Local Tuya.

### Výhody
- Funguje to Lokálne nevyužíva Cloud, nie je potreba žiadny Tuya Convert.
- Funguje to aj počas vypadku (ISP) Internetu.
- Nulová odozva.

### Podporované zariadenie a Appky
- Tuya
- Smart Life
- Vypinače aj dvojtie vypinače atd.
- Prepinače (Switch)
- Zástrčky aj ktoré merajú spotrebu (vrátane tých s ďalšími USB konektormi)
- Svetlá
- Covers
- Fans
- Climates (Čoskoro)

### Problémy a nedostatky
🚨Pokiaľ sa vyskytne dajaký problém alebo dajaký nedostatok tak to spíš do Issues a ti pomôžem stým.

## Mapa
- [1](https://github.com/DzurisHome/LocalTuya#1) Potrebné bez toho sa ďalej *****neposuvneme*****.
- [2](https://github.com/DzurisHome/LocalTuya#21) Získanie *****KEY/KĽUČA***** cez *****[Tuya IoT](https://iot.tuya.com/)*****.
- [3](https://github.com/DzurisHome/LocalTuya/blob/main/README.md#3) Ako pridať *****zariadenia***** do *****Home Assistanta*****.

### 1
Prvé pôjdeme na stránku *****[Tuya IoT](https://iot.tuya.com/)***** tam sa zaregistrujeme a prihlásime potom pôjdeme na položku *****[Cloud](https://iot.tuya.com/cloud/)***** práve vidíme pred sebou *****TRIAL EDITION***** a pod tým je *****Free Trial***** tak na *****Free Trial***** klikneme a sa nám otvorila nová karta a len dáme *****[Buy now](https://github.com/DzurisHome/LocalTuyaSK/blob/main/TRIAL%20EDITION.png)***** a môžme zatvoriť kartu a ísť späť na *****[Cloud](https://iot.tuya.com/cloud/)***** a dať *****F5*****, klikneme na *****Create***** vyplníme potrebné veci ktoré po nás vyžaduje po vyplnený klikneme na *****create*****, práve pred sebou vidíme náš *****Projekt***** ktorý sme vytvorili klikneme na neho vidíme tam *****Authorization Key***** pod tým je *****Access ID/Client ID: fgdfhg41g4ghf***** a *****Access Secret/Client Secret:gh54j5gh4j5gjfhjgh22***** obidve tieto kľúče si niekde okopírujeme, vidíme tam *****[Link Device](https://iot.tuya.com/cloud/appinfo/cappId/device)***** klikneme nato potom klikneme na *****Link devices by App Account***** a ešte klikneme na *****Add App Account***** práve sa nám zobrazil *****QR KOD***** teraz prejdeme do aplikácií čo mame v mobile alebo tablete buď *****(Tuya alebo SmartLife)***** stlačíme to *****plusko***** čo je v právo hore a teraz klikneme na tu malú ikonu čo je úplne hore v právo a teraz môžme oskenoať ten *****QR KOD***** ktorý sa nám ukázal na *****[Tuya IoT](https://iot.tuya.com/)*****, oskenujeme a prepojenie je úspešne, teraz klikneme na *****[Device List](https://iot.tuya.com/cloud/appinfo/cappId/deviceList)***** a vyberieme si *****Európu***** a sa nám zobrazia naše zariadenia ktoré chceme pridať do *****Home Assistant*****, si jeho *****Device Name/ID***** niekde okopírujeme presnejšie je to hneď dole pod názvom zariadenia a teraz prejdeme na *****[Cloud](https://iot.tuya.com/cloud/)***** čo je na ľavo potom klikneme na *****[API Product](https://iot.tuya.com/cloud/appinfo/cappId/setting)***** nájdeme si tam *****[Smart Home Devices Management](https://iot.tuya.com/cloud/ability?abilityId=1365686146595553291)***** klikneme nato a dáme *****[Project](https://iot.tuya.com/cloud/ability?abilityId=1365686146595553291&tab=3)***** vidíme tam  *****New Authorization***** klikneme nato a vyberieme si tam náš *****Projekt***** ktorý sme vytvorili a dáme *****OK*****, a môžme zatvoriť *****Tuya IoT Cloud***** pokiaľ sme si vybrali variantu na získanie *****Key (Kľúčov)***** [2.2 Node.js a CMD](https://github.com/DzurisHome/LocalTuya/blob/main/README.md#22).

![Tuya](https://github.com/milandzuris/LocalTuya/blob/main/Tuya.png)

### 2
Prejdeme v *****[Tuya IoT](https://iot.tuya.com/)***** na *****[Cloud](https://iot.tuya.com/cloud/)***** potom *****[API Explorer](https://iot.tuya.com/cloud/appinfo/cappId/explorer)***** v *****Data Center***** vybereme si našu oblasť napr. *****Europa***** klikneme na *****Get device details***** vidíme tam *****device_id:***** do toho vložíme *****Device Name/ID***** ktorý mame skopirovany a stlačime *****Sumbit Request***** ktorý je dole, práve nám vyšla odpved v *****Response***** pokiaľ nie klikni *****[TU](https://github.com/DzurisHome/LocalTuya/blob/main/README.md#2Cors)*****, skopírujeme si iba *****local_key***** a mame hotové, pokiaľ chceme od ďalšieho zariadenia *****local_key***** urobíme to iste len len použijeme iné *****Device Name/ID*****.

![Tuya](https://github.com/DzurisHome/LocalTuyaSK/blob/main/Tuya%20Square.png)

### 3
Otvoríme si v *****Home Assistantovi [HACS](https://github.com/hacs)***** klikneme na *****Integrations***** vyhľadáme tam *****[Local Tuya](https://github.com/rospogrigio/localtuya)***** nainštalujeme a dáme reštart Home Assistanta, otvoríme si *****Configuration***** dáme integrations klikneme na *****+ ADD INTEGRATION***** vyhľadáme *****LocalTuya***** klikneme na to vybereme si zariadenie ktoré chceme pridať do *****Home Assistantovi***** dáme *****SUMBIT***** nastavíme Meno, do *****Key:***** pridáme tu odpoveď ktorá nám vyšla vo *****CMD/Tuya*****, rovanko v *****CMD***** je to pomenované ako v *****Home Assostantovi***** a v *****Tuya***** je to *****local_key*****, vybereme najnovší protkol dáme *****SUMBIT***** dalej mame tam *****ID***** nastavíme *****1 (value: False)***** len pokiaľ mame iba *****Switch***** alebo obyčajnú *****Zásuvku***** ktorá nemeria nič, pokiaľ chceme niečo iné pridať tak to spravíme podľa toho to *****[TU](https://github.com/DzurisHome/LocalTuya/blob/main/README.md#32)*****, vidíme *****Friendly name***** tam nastavíme meno akým chceme žeby to dane zariadenie bolo pomenované *****Current***** bude *****1 (value: False)***** tiež tak isto *****Current: Consumption***** aj *****Voltage***** a môžme dať *****SUMBIT***** a hotové.

![Local Tuya](https://github.com/milandzuris/LocalTuyaSK/blob/main/Local%20Tuya.png)    ![Home Assistant](https://github.com/DzurisHome/LocalTuyaSK/blob/main/Home%20Assistant.png)


## Social
[<img src='https://img.icons8.com/nolan/64/discord-logo.png' alt='Discord' height='64'>](https://discord.gg/wpg5aAx) [<img src='https://img.icons8.com/nolan/64/instagram-new.png' alt='Instagram' height='64'>](https://instagram.com/dzurishome) [<img src='https://img.icons8.com/nolan/64/twitter.png' alt='Twitter' height='64'>](https://twitter.com/DzurisHome)

### Social Stats
[![Discord Server](https://discord.com/api/guilds/731017969706205264/embed.png)](https://discord.gg/wpg5aAx)

### Repositary Stats
![Issues](https://img.shields.io/github/issues/DzurisHome/LocalTuyaSK?color=FF0000&style=for-the-badge) ![License](https://img.shields.io/github/license/DzurisHome/LocalTuyaSK?style=for-the-badge) ![Forks](https://img.shields.io/github/forks/DzurisHome/LocaltuyaSK?style=for-the-badge) ![Stars](https://img.shields.io/github/stars/DzurisHome/LocalTuyaSK?color=FFE400&style=for-the-badge)  
