# LocalTuya Tutorial SK

Ako integrovať TuYa zariadenia do Home Assistanta cez TuYa Local.

## Výhody
- Funguje to Lokálne nevyužíva to Cloud, neje potreba žiadny Tuya Convert.
- Funguje to aj počas vypadaku (ISP) Internetu.
- Nulová odozva.

## 1.
Prvé pôjdeme na stránku [Tuya IoT](https://iot.tuya.com/ "Tuya IoT") tam sa zaregistrujeme a prihlásime potom pôjdeme na položku *****Cloud***** tam klikneme na *****TRY IT FREE***** a potom na *****Create***** vyplníme potrebné veci, ktoré po nás vyžaduje po vyplnený klikneme na *****create*****, práve pred sebou vidíme náš Projekt ktorý sme vytvorili, klikneme na neho vidíme tam *****Authorization Key***** pod tým je *****Access ID/Client ID: fgdfhg41g4ghf***** a *****Access Secret/Client Secret:gh54j5gh4j5gjfhjgh22***** obidve tieto kľúče si niekde okopírujeme, vidíme tam *****Link Device***** klikneme nato potom klikneme na *****Link devices by App Account***** a ešte klikneme na *****Add App Account***** práve sa nám zobrazil *****QR KOD***** teraz prejdeme do aplikácií, čo mame v mobile alebo tablete stlačíme to plusko, čo je v právo hore a teraz klikneme na tu malú ikonu čo je úplne hore v pravo teraz môžme oskenoať ten *****QR KOD***** ktorý sa nám ukázal na *****Tuya IoT***** oskenujeme a prepojenie je úspešne, teraz klikneme na *****Device List***** a vyberieme si *****Európu***** a sa nám zobrazia naše zariadenia z toho to jedného zariadenia si niekde okopírujeme *****Device Name/ID***** presnejšie je to hneď dole pod názvom zariadenia, a môžme zatvoriť Tuya IoT Cloud.

## 2.
Pojdeme na stranku [Node JS](https://nodejs.org/en/download/ "Node JS") a si stiahneme *****Node.js*****, a si ho nainštalujeme a po inštalacii si otovorime *****Prikazovy Riadok CMD***** a si skopirujeme tam `npm i @tuyapi/cli -g` a dame enter po ukončeni si tam skopirujeme `tuya-cli wizard` a dame enter po dalšiom ukončeni bude to po nas pytať *****The API key from tuya.com:***** skopirujeme tam svoj *****Access ID/Client ID:***** dame enter potom *****Access Secret/Client Secret:***** dame enter bude po nas teraz pytat *****Provide a 'virtual ID' of a device currently registered in the app:***** vložime ho tam a dame zase enter, teraz na nas vyšla odpoved (Kľuče) teraz si to cele niekde okpirujeme a možme CMD vypnut.

## 3.
Otvorime si v *****Home Assistantovi HACS***** klikneme na *****Integrations***** vyhladame tam *****Local Tuya***** nainštalujeme dame reštart Home Assistanta, otvorime si *****Configuration***** dame integrations klikneme na *****+ ADD INTEGRATION***** vyhladame *****LocalTuya***** klikneme na to, vybereme si zariadenie ktore chceme pridat do *****HA***** dame *****SUMBIT***** nastavime Meno do *****Key:***** pridame tu odpoved ktora nam vyšla vo *****CMD***** rovanko v *****CMD***** je to pomenovane ako v HA, vybereme protkol dame *****SUMBIT***** a hotove.
