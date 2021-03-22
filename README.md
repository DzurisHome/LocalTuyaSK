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

## Social
[<img src='https://img.icons8.com/cute-clipart/64/000000/discord-logo.png' alt='Discord' height='64'>](https://discord.gg/wpg5aAx) [<img src='https://img.icons8.com/ios/100/000000/instagram-new--v3.png' alt='Instagram' height='64'>](https://instagram.com/milandzuris) [<img src='https://img.icons8.com/cute-clipart/64/000000/twitter.png' alt='Twitter' height='64'>](https://twitter.com/DzurisHome)

## Stats
[![Discord Server](https://discord.com/api/guilds/731017969706205264/embed.png)](https://discord.gg/wpg5aAx) ![Twitter](https://img.shields.io/twitter/follow/DzurisHome?color=00C1FF&style=for-the-badge)

## Repositary
![Issues](https://img.shields.io/github/issues/DzurisHome/LocalTuya?color=FF0000&style=for-the-badge) ![License](https://img.shields.io/github/license/DzurisHome/LocalTuya?style=for-the-badge) ![Forks](https://img.shields.io/github/forks/DzurisHome/Localtuya?style=for-the-badge) ![Stars](https://img.shields.io/github/stars/DzurisHome/LocalTuya?color=FFE400&style=for-the-badge)  











[<svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px"
width="64" height="64"
viewBox="0 0 172 172"
style=" fill:#000000;"><defs><linearGradient x1="86" y1="17.91756" x2="86" y2="155.531" gradientUnits="userSpaceOnUse" id="color-1_43625_gr1"><stop offset="0" stop-color="#00c6ff"></stop><stop offset="1" stop-color="#0072ff"></stop></linearGradient><linearGradient x1="86" y1="48.82381" x2="86" y2="122.76231" gradientUnits="userSpaceOnUse" id="color-2_43625_gr2"><stop offset="0" stop-color="#70dfff"></stop><stop offset="1" stop-color="#70afff"></stop></linearGradient><linearGradient x1="123.625" y1="34.26563" x2="123.625" y2="61.94419" gradientUnits="userSpaceOnUse" id="color-3_43625_gr3"><stop offset="0" stop-color="#70dfff"></stop><stop offset="1" stop-color="#70afff"></stop></linearGradient></defs><g fill="none" fill-rule="nonzero" stroke="none" stroke-width="1" stroke-linecap="butt" stroke-linejoin="miter" stroke-miterlimit="10" stroke-dasharray="" stroke-dashoffset="0" font-family="none" font-weight="none" font-size="none" text-anchor="none" style="mix-blend-mode: normal"><path d="M0,172v-172h172v172z" fill="none"></path><g><path d="M118.25,153.1875h-64.5c-19.264,0 -34.9375,-15.6735 -34.9375,-34.9375v-64.5c0,-19.264 15.6735,-34.9375 34.9375,-34.9375h64.5c19.264,0 34.9375,15.6735 34.9375,34.9375v64.5c0,19.264 -15.6735,34.9375 -34.9375,34.9375zM53.75,24.1875c-16.29969,0 -29.5625,13.26281 -29.5625,29.5625v64.5c0,16.29969 13.26281,29.5625 29.5625,29.5625h64.5c16.29969,0 29.5625,-13.26281 29.5625,-29.5625v-64.5c0,-16.29969 -13.26281,-29.5625 -29.5625,-29.5625z" fill="url(#color-1_43625_gr1)"></path><path d="M86,120.9375c-19.264,0 -34.9375,-15.6735 -34.9375,-34.9375c0,-19.264 15.6735,-34.9375 34.9375,-34.9375c19.264,0 34.9375,15.6735 34.9375,34.9375c0,19.264 -15.6735,34.9375 -34.9375,34.9375zM86,61.8125c-13.33537,0 -24.1875,10.85213 -24.1875,24.1875c0,13.33806 10.85213,24.1875 24.1875,24.1875c13.33806,0 24.1875,-10.84944 24.1875,-24.1875c0,-13.33537 -10.84944,-24.1875 -24.1875,-24.1875z" fill="url(#color-2_43625_gr2)"></path><path d="M123.625,40.3125c-4.4528,0 -8.0625,3.6097 -8.0625,8.0625c0,4.4528 3.6097,8.0625 8.0625,8.0625c4.4528,0 8.0625,-3.6097 8.0625,-8.0625c0,-4.4528 -3.6097,-8.0625 -8.0625,-8.0625z" fill="url(#color-3_43625_gr3)"></path></g></g></svg> alt='Discord' height='64'>](https://twitter.com/DzurisHome)
