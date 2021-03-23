# Local Tuya Tutorial SK

## Ako integrovať TuYa zariadenia do Home Assistanta cez Tuya Local.

![Dzuriš Home, Local Tuya, Tuya](https://github.com/DzurisHome/LocalTuya/blob/main/0.1.jpg)

[<img src='https://img.icons8.com/nolan/64/discord-logo.png' alt='Discord' height='64'>](https://discord.gg/wpg5aAx) [<img src='https://img.icons8.com/nolan/64/instagram-new.png' alt='Instagram' height='64'>](https://instagram.com/milandzuris) [<img src='https://img.icons8.com/nolan/64/twitter.png' alt='Twitter' height='64'>](https://twitter.com/DzurisHome)

## Výhody
- Funguje to Lokálne nevyužíva to Cloud, neje potreba žiadny Tuya Convert.
- Funguje to aj počas vypadaku (ISP) Internetu.
- Nulová odozva.

## Rozspis
- [1](https://github.com/DzurisHome/LocalTuya#1) Potrebné bez toho sa ďalej neposuvneme.
- [2.1](https://github.com/DzurisHome/LocalTuya#21) Rýchlejšie získanie *****KEY/KĽUČA*****.
- [2.Cors](https://github.com/DzurisHome/LocalTuya#2cors) Môže sa stáť že sa nám neukáže odpoveď v *****[2.1](https://github.com/DzurisHome/LocalTuya#21)***** tak bude treba *****Cors***** ktorý iba funguje na *****Chromium prehladačoch*****.
- [3](https://github.com/DzurisHome/LocalTuya#3) Pomalšie získanie *****KEY/KĽUČA***** ale môžme získať na par kliky všetky naraz kľúče a plus je potreba nainštalovať iba Node.js

## 1
Prvé pôjdeme na stránku *****[Tuya IoT](https://iot.tuya.com/)***** tam sa zaregistrujeme a prihlásime potom pôjdeme na položku *****[Cloud](https://iot.tuya.com/cloud/)***** tam klikneme na *****TRY IT FREE***** a potom na *****Create***** vyplníme potrebné veci, ktoré po nás vyžaduje po vyplnený klikneme na *****create*****, práve pred sebou vidíme náš *****Projekt***** ktorý sme vytvorili, klikneme na neho vidíme tam *****Authorization Key***** pod tým je *****Access ID/Client ID: fgdfhg41g4ghf***** a *****Access Secret/Client Secret:gh54j5gh4j5gjfhjgh22***** obidve tieto kľúče si niekde okopírujeme, vidíme tam *****[Link Device](https://iot.tuya.com/cloud/appinfo/cappId/device)***** klikneme nato potom klikneme na *****Link devices by App Account***** a ešte klikneme na *****Add App Account***** práve sa nám zobrazil *****QR KOD***** teraz prejdeme do aplikácií čo mame v mobile alebo tablete buď *****(Tuya alebo SmartLife)***** stlačíme to *****plusko***** čo je v právo hore a teraz klikneme na tu malú ikonu čo je úplne hore v pravo a teraz môžme oskenoať ten *****QR KOD***** ktorý sa nám ukázal na *****[Tuya IoT](https://iot.tuya.com/)*****, oskenujeme a prepojenie je úspešne, teraz klikneme na *****[Device List](https://iot.tuya.com/cloud/appinfo/cappId/deviceList)***** a vyberieme si *****Európu***** a sa nám zobrazia naše zariadenia ktoré chceme pridať do *****Home Assistant*****, si jeho *****Device Name/ID***** niekde okopírujeme presnejšie je to hneď dole pod názvom zariadenia a teraz prejdeme na *****[Cloud](https://iot.tuya.com/cloud/)***** čo je na ľavo potom klikneme na *****[API Product](shttps://iot.tuya.com/cloud/appinfo/cappId/setting)***** nájdeme si tam *****[Smart Home Devices Management](https://iot.tuya.com/cloud/ability?abilityId=1365686146595553291)***** klikneme nato a dáme *****[Project](shttps://iot.tuya.com/cloud/ability?abilityId=1365686146595553291&tab=3)***** vidíme tam  *****New Authorization***** klikneme nato a vyberieme si tam náš *****Projekt***** ktorý sme vytvorili a dáme *****OK*****, a môžme zatvoriť *****Tuya IoT Cloud***** pokiaľ sme si vybrali variantu na získanie *****Key (Kľúčov)***** [2.2 Node.js a CMD](https://github.com/DzurisHome/LocalTuya/blob/main/README.md#22).

![Tuya](https://github.com/milandzuris/LocalTuya/blob/main/Tuya.png)

## 2.1
Prejdeme v *****[Tuya IoT](https://iot.tuya.com/)***** na *****[Cloud](https://iot.tuya.com/cloud/)***** potom *****[API Explorer](https://iot.tuya.com/cloud/appinfo/cappId/explorer)***** v *****Data Center***** vybereme si našu oblasť napr. *****Europa***** klikneme na *****Get device details***** vidíme tam *****device_id:***** do toho vložíme *****Device Name/ID***** ktorý mame okopirovany a stalčime *****Sumbit Request***** ktory je dole, práve nám vyšla odpved v *****Response***** pokiaľ nie klikni *****[TU](https://github.com/DzurisHome/LocalTuya/blob/main/README.md#2Cors)*****, okopírujeme si iba *****local_key***** a mame hotové, pokiaľ chceme od dalšieho zariadenia *****local_key***** urobíme to iste len len použijeme iné *****Device Name/ID*****.


### 2.Cors
Nainštalujeme si *****[Cors](https://chrome.google.com/webstore/detail/allow-cors-access-control/lhobafahddgcelffkeicbaginigeejlf)***** potom klikneme hore v pravo na *****Cors***** a dame *****Toggle ON***** a prejdem spat na *****[Tuya IoT](https://iot.tuya.com/)***** a dame *****F5*****, prejdeme na *****[Cloud](https://iot.tuya.com/cloud/)***** potom *****[API Explorer](https://iot.tuya.com/cloud/appinfo/cappId/explorer)***** v *****Data Center***** vybereme si našu oblasť napr. *****Europa***** klikneme na *****Get device details***** vidíme tam *****device_id:***** do toho vložíme *****Device Name/ID***** ktorý mame okopirovany a stalčime *****Sumbit Request***** ktory je dole, práve nám vyšla odpved v *****Response***** a okopírujeme si iba *****local_key***** a mame hotové, pokiaľ chceme od dalšieho zariadenia *****local_key***** urobíme to iste len len použijeme iné *****Device Name/ID*****.
#### Cors funguje iba na Chromium prehlidačoch

## 2.2
Pôjdeme na stránku [Node.js](https://nodejs.org/en/download/ "Node.js") a si stiahneme *****Node.js*****, a si ho nainštalujeme a po inštalácii si otovorime *****Príkazový Riadok CMD***** a si skopírujeme tam `npm i @tuyapi/cli -g` a dáme enter po ukončení si tam skopírujeme `tuya-cli wizard` a dáme enter po dalšiom ukončení bude to po nás pýtať *****The API key from tuya.com:***** skopírujeme tam svoj *****Access ID/Client ID:***** dáme enter potom *****Access Secret/Client Secret:***** dáme enter bude po nás teraz pýtať *****Provide a 'virtual ID' of a device currently registered in the app:***** vložíme ho tam a dáme zase enter, teraz na nás vyšla odpoveď (Kľúče) teraz si to cele niekde okpirujeme a môžme CMD vypnúť.

![Node JS](https://github.com/DzurisHome/LocalTuya/blob/main/Node%20JS.png)    ![Terminal](https://github.com/DzurisHome/LocalTuya/blob/main/Terminal.png)

## 3
Otvoríme si v *****Home Assistantovi [HACS](https://github.com/hacs)***** klikneme na *****Integrations***** vyhľadáme tam *****[Local Tuya](https://github.com/rospogrigio/localtuya)***** nainštalujeme a dáme reštart Home Assistanta, otvoríme si *****Configuration***** dáme integrations klikneme na *****+ ADD INTEGRATION***** vyhľadáme *****LocalTuya***** klikneme na to vybereme si zariadenie ktoré chceme pridať do *****HA***** dáme *****SUMBIT***** nastavíme Meno do *****Key:***** pridáme tu odpoveď ktorá nám vyšla vo *****CMD*****, rovanko v *****CMD***** je to pomenované ako v HA, vybereme protkol dáme *****SUMBIT***** dalej mame tam *****ID***** nastavime *****1 (value: False)***** vidime *****Friendly name***** tam nastavime meno akym chceme žeby to dane zariadenie bolo pomenovane *****Current***** bude *****1 (value: False)***** tiež tak isto *****Current: Consumption***** aj *****Voltage***** a možme dat *****SUMBIT*****  a hotové.

![Local Tuya](https://github.com/milandzuris/LocalTuya/blob/main/Local%20Tuya.png)    ![Home Assistant](https://github.com/DzurisHome/LocalTuya/blob/main/Home%20Assistant.png)

## Social
[<img src='https://img.icons8.com/nolan/64/discord-logo.png' alt='Discord' height='64'>](https://discord.gg/wpg5aAx) [<img src='https://img.icons8.com/nolan/64/instagram-new.png' alt='Instagram' height='64'>](https://instagram.com/milandzuris) [<img src='https://img.icons8.com/nolan/64/twitter.png' alt='Twitter' height='64'>](https://twitter.com/DzurisHome)

## Stats
[![Discord Server](https://discord.com/api/guilds/731017969706205264/embed.png)](https://discord.gg/wpg5aAx) ![Twitter](https://img.shields.io/twitter/follow/DzurisHome?color=00C1FF&style=for-the-badge)

## Repositary
![Issues](https://img.shields.io/github/issues/DzurisHome/LocalTuya?color=FF0000&style=for-the-badge) ![License](https://img.shields.io/github/license/DzurisHome/LocalTuya?style=for-the-badge) ![Forks](https://img.shields.io/github/forks/DzurisHome/Localtuya?style=for-the-badge) ![Stars](https://img.shields.io/github/stars/DzurisHome/LocalTuya?color=FFE400&style=for-the-badge)  
