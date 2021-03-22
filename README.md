# Local Tuya Tutorial SK

## Ako integrovať TuYa zariadenia do Home Assistanta cez Tuya Local.

![Dzuriš Home, Local Tuya, Tuya](https://github.com/DzurisHome/LocalTuya/blob/main/0.1.jpg)

[<img src='https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/instagram.svg' alt='instagram' height='60'>](https://www.instagram.com/DzurisHome/)  [<img src='https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/twitter.svg' alt='twitter' height='60'>](https://twitter.com/DzurisHome)  [<img src='https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/discord.svg' alt='discord' height='60'>](https://discord.gg/wpg5aAx)  

## Výhody
- Funguje to Lokálne nevyužíva to Cloud, neje potreba žiadny Tuya Convert.
- Funguje to aj počas vypadaku (ISP) Internetu.
- Nulová odozva.

## 1.
Prvé pôjdeme na stránku [Tuya IoT](https://iot.tuya.com/ "Tuya IoT") tam sa zaregistrujeme a prihlásime potom pôjdeme na položku *****Cloud***** tam klikneme na *****TRY IT FREE***** a potom na *****Create***** vyplníme potrebné veci, ktoré po nás vyžaduje po vyplnený klikneme na *****create*****, práve pred sebou vidíme náš Projekt ktorý sme vytvorili, klikneme na neho vidíme tam *****Authorization Key***** pod tým je *****Access ID/Client ID: fgdfhg41g4ghf***** a *****Access Secret/Client Secret:gh54j5gh4j5gjfhjgh22***** obidve tieto kľúče si niekde okopírujeme, vidíme tam *****Link Device***** klikneme nato potom klikneme na *****Link devices by App Account***** a ešte klikneme na *****Add App Account***** práve sa nám zobrazil *****QR KOD***** teraz prejdeme do aplikácií, čo mame v mobile alebo tablete stlačíme to plusko, čo je v právo hore a teraz klikneme na tu malú ikonu čo je úplne hore v pravo teraz môžme oskenoať ten *****QR KOD***** ktorý sa nám ukázal na *****Tuya IoT***** oskenujeme a prepojenie je úspešne, teraz klikneme na *****Device List***** a vyberieme si *****Európu***** a sa nám zobrazia naše zariadenia z toho to jedného zariadenia si niekde okopírujeme *****Device Name/ID***** presnejšie je to hneď dole pod názvom zariadenia, a môžme zatvoriť Tuya IoT Cloud.

![Tuya](https://github.com/milandzuris/LocalTuya/blob/main/Tuya.png)

## 2.
Pôjdeme na stránku [Node JS](https://nodejs.org/en/download/ "Node JS") a si stiahneme *****Node.js*****, a si ho nainštalujeme a po inštalácii si otovorime *****Príkazový Riadok CMD***** a si skopírujeme tam `npm i @tuyapi/cli -g` a dáme enter po ukončení si tam skopírujeme `tuya-cli wizard` a dáme enter po dalšiom ukončení bude to po nás pýtať *****The API key from tuya.com:***** skopírujeme tam svoj *****Access ID/Client ID:***** dáme enter potom *****Access Secret/Client Secret:***** dáme enter bude po nás teraz pýtať *****Provide a 'virtual ID' of a device currently registered in the app:***** vložíme ho tam a dáme zase enter, teraz na nás vyšla odpoveď (Kľúče) teraz si to cele niekde okpirujeme a môžme CMD vypnúť.

![Node JS](https://github.com/DzurisHome/LocalTuya/blob/main/Node%20JS.png)    ![Terminal](https://github.com/DzurisHome/LocalTuya/blob/main/Terminal.png)

## 3.
Otvoríme si v *****Home Assistantovi HACS***** klikneme na *****Integrations***** vyhľadáme tam *****Local Tuya***** nainštalujeme a dáme reštart Home Assistanta, otvoríme si *****Configuration***** dáme integrations klikneme na *****+ ADD INTEGRATION***** vyhľadáme *****LocalTuya***** klikneme na to, vybereme si zariadenie ktoré chceme pridať do *****HA***** dáme *****SUMBIT***** nastavíme Meno do *****Key:***** pridáme tu odpoveď ktorá nám vyšla vo *****CMD*****, rovanko v *****CMD***** je to pomenované ako v HA, vybereme protkol dáme *****SUMBIT***** a hotové.

![Local Tuya](https://github.com/milandzuris/LocalTuya/blob/main/Local%20Tuya.png)    ![Home Assistant](https://github.com/DzurisHome/LocalTuya/blob/main/Home%20Assistant.png)

## 4.

![Issues](https://img.shields.io/codeclimate/issues/DzurisHome/LocalTuya?style=for-the-badge)

[<img src='https://img.icons8.com/cute-clipart/64/000000/discord-logo.png' alt='Discord' height='64'>](https://discord.gg/wpg5aAx) ![Discord Online](https://img.shields.io/discord/731017969706205264?style=flat-square)
