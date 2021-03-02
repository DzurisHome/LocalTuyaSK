# LocalTuya Tutorial SK

Ako integrovať TuYa Cloud zariadenia cez TuYa Local do Home Assistanta

## Vyhody
- Funguje to Lokalne nevyuživa to Cloud, neje potreba žiadny Tuya Convert.
- Funguje to aj počas vypadaku (ISP) Internetu.
- Nulova odozva.

## 1.
Prve pojdeme na stranku [Tuya IoT Cloud](https://iot.tuya.com/ "Tuya IoT Cloud") tam sa zaregistrujeme a prihlasime potom pojdeme na položku ****Cloud**** tam klikneme na ****TRY IT FREE**** a potom na ****Create**** vyplnime potrebne veci ktore po nas vyžaduje po vyplneni klikneme na ****create****, prave pred sebou vidime naš Projekt ktory sme vytvorili, klikneme na neho vidime tam ***Authorization Key*** pod tym je ***Access ID/Client ID: fgdfhg41g4ghf*** a ***Access Secret/Client Secret:gh54j5gh4j5gjfhjgh22*** obidve tieto kľuce si niekde okopirujeme, vidime tam ****Link Device**** klikneme nato potom klikneme na ****Link devices by App Account**** a ešte klikneme na ****Add App Account**** prave sa nam zobrazil ***QR KOD*** teraz prejdeme do aplikacii čo mame v mobile alebo tablete stlačime to plusko čo je v pravo hore a teraz klikneme na tu malu ikonu čo je uplne hore v pravo teraz možme oskenoať ten ****QR KOD**** ktory sa nam ukazal na ***Tuya IoT Cloude*** oskenujeme a prepojenie je uspešne.

## 2.
Pojdeme na stranku [Node JS](https://nodejs.org/en/download/ "Node JS") a si stiahneme Node.js, a si to nainštalujeme a pot inštalacii si otovorime ****Praikozvy Riadok CMD**** a s skopirujeme si tam `npm i @tuyapi/cli -g` po ukončeni si zase tam skopirujeme `tuya-cli wizard`
