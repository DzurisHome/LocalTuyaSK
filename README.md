# LocalTuya Tutorial SK

Ako integrovať TuYa Cloud zariadenia cez TuYa Local do Home Assistanta

## Vyhody
- Funguje to Lokalne nevyuživa to Cloud, neje potreba žiadny Tuya Convert.
- Funguje to aj počas vypadaku (ISP) Internetu.
- Nulova odozva.

## 1.
Prve pojdeme na stranku [Tuya IoT Cloud](https://iot.tuya.com/ "Tuya IoT Cloud") tam sa zaregistrujeme a prihlasime potom pojdeme na položku ****Cloud**** tam klikneme na ****TRY IT FREE**** a potom na ****Create**** vyplnime potrebne veci ktore po nas vyžaduje po vyplneni klikneme na ****create****, prave pred sebou vidime naš Projekt ktory sme vytvorili, klikneme na neho vidime tam ***Authorization Key*** pod tym je ***Access ID/Client ID: fgdfhg41g4ghf*** a ***Access Secret/Client Secret:gh54j5gh4j5gjfhjgh22*** obidve tieto kľuce si niekde okopirujeme, vidime tam ****Link Device**** klikneme nato potom klikneme na ****Link devices by App Account**** a ešte klikneme na ****Add App Account**** prave sa nam zobrazil ***QR KOD*** teraz prejdeme do aplikacii čo mame v mobile alebo tablete stlačime to plusko čo je v pravo hore a teraz klikneme na tu malu ikonu čo je uplne hore v pravo teraz možme oskenoať ten ****QR KOD**** ktory sa nam ukazal na ***Tuya IoT Cloude*** oskenujeme a prepojenie je uspešne, teraz klikneme na ***Device List*** a vybereme si ***Europu*** a sa nam zobrazia naše zariadenia z toho to jedneho zariadenia si niekde okopirujeme ***Device Name/ID*** presnejšie je to hned dole pod nazvom zariadenia, a možme zatvorit Tuya IoT Cloud.

## 2.
Pojdeme na stranku [Node JS](https://nodejs.org/en/download/ "Node JS") a si stiahneme Node.js, a si ho nainštalujeme a po inštalacii si otovorime ****Prikazovy Riadok CMD**** a si skopirujeme tam `npm i @tuyapi/cli -g` a dame enter po ukončeni si tam skopirujeme `tuya-cli wizard` a dame enter po dalšiom ukončeni bude to po nas pytať ****The API key from tuya.com:**** skopirujeme tam svoj ***Access ID/Client ID:*** dame enter potom ***Access Secret/Client Secret:*** dame enter bude po nas teraz pytat ***Provide a 'virtual ID' of a device currently registered in the app:*** vložime ho tam a dame zase enter, teraz na nas vyšla odpoved (Kľuče) teraz si to cele niekde okpirujeme a možme CMD vypnut.

## 3.
Otvorime si v ****Home Assistantovi HACS**** klikneme na ***Integrations*** vyhladame tam ****Local Tuya**** nainštalujeme dame reštart Home Assistanta, otvorime si ***Configuration*** dame integrations klikneme na ****+ ADD INTEGRATION**** vyhladame ****LocalTuya*** klikneme na to, vybereme si zariadenie ktore chceme pridat do ***HA*** dame ***SUMBIT*** nastavime Meno do ***Key:*** pridame tu odpoved ktora nam vyšla vo ***CMD*** rovanko v ***CMD*** je to pomenovane vybereme protkol dame ***SUMBIT*** a hotove.
