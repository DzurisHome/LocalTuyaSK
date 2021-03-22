# Local Tuya Tutorial SK

## Ako integrovať TuYa zariadenia do Home Assistanta cez Tuya Local.

![Dzuriš Home, Local Tuya, Tuya](https://github.com/DzurisHome/LocalTuya/blob/main/0.1.jpg)

[<img src='https://img.icons8.com/nolan/64/discord-logo.png' alt='Discord' height='64'>](https://discord.gg/wpg5aAx) [<img src='https://img.icons8.com/nolan/64/instagram-new.png' alt='Instagram' height='64'>](https://instagram.com/milandzuris) [<img src='https://img.icons8.com/nolan/64/twitter.png' alt='Twitter' height='64'>](https://twitter.com/DzurisHome)

## Výhody
- Funguje to Lokálne nevyužíva to Cloud, neje potreba žiadny Tuya Convert.
- Funguje to aj počas vypadaku (ISP) Internetu.
- Nulová odozva.

## 1.
Prvé pôjdeme na stránku [Tuya IoT](https://iot.tuya.com/ "Tuya IoT") tam sa zaregistrujeme a prihlásime potom pôjdeme na položku *****Cloud***** tam klikneme na *****TRY IT FREE***** a potom na *****Create***** vyplníme potrebné veci, ktoré po nás vyžaduje po vyplnený klikneme na *****create*****, práve pred sebou vidíme náš Projekt ktorý sme vytvorili, klikneme na neho vidíme tam *****Authorization Key***** pod tým je *****Access ID/Client ID: fgdfhg41g4ghf***** a *****Access Secret/Client Secret:gh54j5gh4j5gjfhjgh22***** obidve tieto kľúče si niekde okopírujeme, vidíme tam *****Link Device***** klikneme nato potom klikneme na *****Link devices by App Account***** a ešte klikneme na *****Add App Account***** práve sa nám zobrazil *****QR KOD***** teraz prejdeme do aplikácií, čo mame v mobile alebo tablete stlačíme to plusko, čo je v právo hore a teraz klikneme na tu malú ikonu čo je úplne hore v pravo teraz môžme oskenoať ten *****QR KOD***** ktorý sa nám ukázal na *****Tuya IoT*****, oskenujeme a prepojenie je úspešne, teraz klikneme na *****Device List***** a vyberieme si *****Európu***** a sa nám zobrazia naše zariadenia, zariadenie ktoré chceme pridať do Home Assistant si jeho *****Device Name/ID***** niekde okopírujeme presnejšie je to hneď dole pod názvom zariadenia, a môžme zatvoriť Tuya IoT Cloud pokiaľ sme si vybrali variantu na získanie Key (Kľúčov) Node.js a CMD.

![Tuya](https://github.com/milandzuris/LocalTuya/blob/main/Tuya.png)

## 2.
Pôjdeme na stránku [Node.js](https://nodejs.org/en/download/ "Node.js") a si stiahneme *****Node.js*****, a si ho nainštalujeme a po inštalácii si otovorime *****Príkazový Riadok CMD***** a si skopírujeme tam `npm i @tuyapi/cli -g` a dáme enter po ukončení si tam skopírujeme `tuya-cli wizard` a dáme enter po dalšiom ukončení bude to po nás pýtať *****The API key from tuya.com:***** skopírujeme tam svoj *****Access ID/Client ID:***** dáme enter potom *****Access Secret/Client Secret:***** dáme enter bude po nás teraz pýtať *****Provide a 'virtual ID' of a device currently registered in the app:***** vložíme ho tam a dáme zase enter, teraz na nás vyšla odpoveď (Kľúče) teraz si to cele niekde okpirujeme a môžme CMD vypnúť.

![Node JS](https://github.com/DzurisHome/LocalTuya/blob/main/Node%20JS.png)    ![Terminal](https://github.com/DzurisHome/LocalTuya/blob/main/Terminal.png)

## 3.
Otvoríme si v *****Home Assistantovi HACS***** klikneme na *****Integrations***** vyhľadáme tam *****Local Tuya***** nainštalujeme a dáme reštart Home Assistanta, otvoríme si *****Configuration***** dáme integrations klikneme na *****+ ADD INTEGRATION***** vyhľadáme *****LocalTuya***** klikneme na to vybereme si zariadenie ktoré chceme pridať do *****HA***** dáme *****SUMBIT***** nastavíme Meno do *****Key:***** pridáme tu odpoveď ktorá nám vyšla vo *****CMD*****, rovanko v *****CMD***** je to pomenované ako v HA, vybereme protkol dáme *****SUMBIT***** dalej mame tam *****ID***** nastavime *****1 (value: False)***** vidime *****Friendly name***** tam nastavime meno akym chceme žeby to dane zariadenie bolo pomenovane *****Current***** bude *****1 (value: False)***** tiež tak isto *****Current: Consumption***** aj *****Voltage***** a možme dat *****SUMBIT*****  a hotové.

![Local Tuya](https://github.com/milandzuris/LocalTuya/blob/main/Local%20Tuya.png)    ![Home Assistant](https://github.com/DzurisHome/LocalTuya/blob/main/Home%20Assistant.png)

## Social
[<img src='https://img.icons8.com/nolan/64/discord-logo.png' alt='Discord' height='64'>](https://discord.gg/wpg5aAx) [<img src='https://img.icons8.com/nolan/64/instagram-new.png' alt='Instagram' height='64'>](https://instagram.com/milandzuris) [<img src='https://img.icons8.com/nolan/64/twitter.png' alt='Twitter' height='64'>](https://twitter.com/DzurisHome)

## Stats
[![Discord Server](https://discord.com/api/guilds/731017969706205264/embed.png)](https://discord.gg/wpg5aAx) ![Twitter](https://img.shields.io/twitter/follow/DzurisHome?color=00C1FF&style=for-the-badge)

## Repositary
![Issues](https://img.shields.io/github/issues/DzurisHome/LocalTuya?color=FF0000&style=for-the-badge) ![License](https://img.shields.io/github/license/DzurisHome/LocalTuya?style=for-the-badge) ![Forks](https://img.shields.io/github/forks/DzurisHome/Localtuya?style=for-the-badge) ![Stars](https://img.shields.io/github/stars/DzurisHome/LocalTuya?color=FFE400&style=for-the-badge)  
