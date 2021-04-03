# Local Tuya Tutorial SK

## Ako integrovať Tuya zariadenia do Home Assistanta cez Local Tuya.

![Dzuriš Home, Local Tuya, Tuya](https://github.com/DzurisHome/LocalTuya/blob/main/0.1.jpg)

[<img src='https://img.icons8.com/nolan/64/discord-logo.png' alt='Discord' height='64'>](https://discord.gg/wpg5aAx) [<img src='https://img.icons8.com/nolan/64/instagram-new.png' alt='Instagram' height='64'>](https://instagram.com/dzurishome) [<img src='https://img.icons8.com/nolan/64/twitter.png' alt='Twitter' height='64'>](https://twitter.com/DzurisHome)

## Výhody
- Funguje to Lokálne nevyužíva to Cloud, nie je potreba žiadny Tuya Convert.
- Funguje to aj počas vypadku (ISP) Internetu.
- Nulová odozva.

## Podporované zariadenie a Appky
- Tuya
- Smart Life
- Vypinače aj dvojtie vypinače atd.
- Prepinače (Switch)
- Zástrčky aj ktoré merajú spotrebu (vrátane tých s ďalšími USB konektormi)
- Svetlá
- Covers
- Fans
- Climates (Čoskoro)

## Problémy a nedostatky
🚨Pokiaľ sa vyskytne dajaký problém alebo dajaký nedostatok tak sa pripoj *****[TU](https://discord.gg/Z9q3SnerWa)***** na Discord a tam to spíš a ti pomôžem stým.
### 🚨Pokiaľ nepôjde niečo z *****YAML Configu***** alebo budú fungovať aj tie YAML Kody ktoré nesú overené *****Fajkou***** tak mi to prosím napíš na Discord alebo do správy na Facebook, pokiaľ niečo čo neje overené a ti to pôjde tak mi pošli screen z YAML Kodu alebo okopíruj ďakujem.

## Mapa
- [1](https://github.com/DzurisHome/LocalTuya#1) Potrebné bez toho sa ďalej *****neposuvneme*****.
- [2.1](https://github.com/DzurisHome/LocalTuya#21) Získanie *****KEY/KĽUČA***** cez *****[Tuya IoT](https://iot.tuya.com/)*****.
- [2.Cors](https://github.com/DzurisHome/LocalTuya#2cors) Môže sa stáť že sa nám neukáže odpoveď v *****[2.1](https://github.com/DzurisHome/LocalTuya#21)***** tak bude treba *****Cors***** ktorý iba funguje na *****Chromium prehladačoch*****.
- [2.2](https://github.com/DzurisHome/LocalTuya#2.2) Rýchlejšie získanie *****KEY/KĽUČA*****, môžme získať na par kliky všetky naraz kľúče a plus je potreba nainštalovať iba *****Node.js*****.
- [3](https://github.com/DzurisHome/LocalTuya/blob/main/README.md#3) Ako pridať *****zariadenia***** do *****Home Assistanta*****.
- [3.2](https://github.com/DzurisHome/LocalTuya/blob/main/README.md#32) Ako nastaviť *****ID, Current, Current Consumption, Voltage***** pokiaľ mame niečo iné ako *****Switch***** a obyčajnú *****Zásuvku***** čo nič nemera.

## 1
Prvé pôjdeme na stránku *****[Tuya IoT](https://iot.tuya.com/)***** tam sa zaregistrujeme a prihlásime potom pôjdeme na položku *****[Cloud](https://iot.tuya.com/cloud/)***** práve vidíme pred sebou *****TRIAL EDITION***** a pod tým je *****Free Trial***** tak na *****Free Trial***** klikneme a sa nám otvorila nová karta a len dáme *****[Buy now](https://github.com/DzurisHome/LocalTuyaSK/blob/main/TRIAL%20EDITION.png)***** a môžme zatvoriť kartu a ísť späť na *****[Cloud](https://iot.tuya.com/cloud/)***** a dať *****F5*****, klikneme na *****Create***** vyplníme potrebné veci ktoré po nás vyžaduje po vyplnený klikneme na *****create*****, práve pred sebou vidíme náš *****Projekt***** ktorý sme vytvorili klikneme na neho vidíme tam *****Authorization Key***** pod tým je *****Access ID/Client ID: fgdfhg41g4ghf***** a *****Access Secret/Client Secret:gh54j5gh4j5gjfhjgh22***** obidve tieto kľúče si niekde okopírujeme, vidíme tam *****[Link Device](https://iot.tuya.com/cloud/appinfo/cappId/device)***** klikneme nato potom klikneme na *****Link devices by App Account***** a ešte klikneme na *****Add App Account***** práve sa nám zobrazil *****QR KOD***** teraz prejdeme do aplikácií čo mame v mobile alebo tablete buď *****(Tuya alebo SmartLife)***** stlačíme to *****plusko***** čo je v právo hore a teraz klikneme na tu malú ikonu čo je úplne hore v právo a teraz môžme oskenoať ten *****QR KOD***** ktorý sa nám ukázal na *****[Tuya IoT](https://iot.tuya.com/)*****, oskenujeme a prepojenie je úspešne, teraz klikneme na *****[Device List](https://iot.tuya.com/cloud/appinfo/cappId/deviceList)***** a vyberieme si *****Európu***** a sa nám zobrazia naše zariadenia ktoré chceme pridať do *****Home Assistant*****, si jeho *****Device Name/ID***** niekde okopírujeme presnejšie je to hneď dole pod názvom zariadenia a teraz prejdeme na *****[Cloud](https://iot.tuya.com/cloud/)***** čo je na ľavo potom klikneme na *****[API Product](https://iot.tuya.com/cloud/appinfo/cappId/setting)***** nájdeme si tam *****[Smart Home Devices Management](https://iot.tuya.com/cloud/ability?abilityId=1365686146595553291)***** klikneme nato a dáme *****[Project](https://iot.tuya.com/cloud/ability?abilityId=1365686146595553291&tab=3)***** vidíme tam  *****New Authorization***** klikneme nato a vyberieme si tam náš *****Projekt***** ktorý sme vytvorili a dáme *****OK*****, a môžme zatvoriť *****Tuya IoT Cloud***** pokiaľ sme si vybrali variantu na získanie *****Key (Kľúčov)***** [2.2 Node.js a CMD](https://github.com/DzurisHome/LocalTuya/blob/main/README.md#22).

![Tuya](https://github.com/milandzuris/LocalTuya/blob/main/Tuya.png)

## 2.1
Prejdeme v *****[Tuya IoT](https://iot.tuya.com/)***** na *****[Cloud](https://iot.tuya.com/cloud/)***** potom *****[API Explorer](https://iot.tuya.com/cloud/appinfo/cappId/explorer)***** v *****Data Center***** vybereme si našu oblasť napr. *****Europa***** klikneme na *****Get device details***** vidíme tam *****device_id:***** do toho vložíme *****Device Name/ID***** ktorý mame okopirovany a stalčime *****Sumbit Request***** ktorý je dole, práve nám vyšla odpved v *****Response***** pokiaľ nie klikni *****[TU](https://github.com/DzurisHome/LocalTuya/blob/main/README.md#2Cors)*****, okopírujeme si iba *****local_key***** a mame hotové, pokiaľ chceme od ďalšieho zariadenia *****local_key***** urobíme to iste len len použijeme iné *****Device Name/ID*****.

![Tuya](https://github.com/DzurisHome/LocalTuyaSK/blob/main/Tuya%20Square.png)

### 2.Cors
Nainštalujeme si *****[Cors](http://bit.ly/DzurišHomeCors)***** potom klikneme hore v právo na *****Cors***** a dáme *****Toggle ON***** a prejdem späť na *****[Tuya IoT](https://iot.tuya.com/)***** a dáme *****F5*****, prejdeme na *****[Cloud](https://iot.tuya.com/cloud/)***** potom *****[API Explorer](https://iot.tuya.com/cloud/appinfo/cappId/explorer)***** v *****Data Center***** vybereme si našu oblasť napr. *****Europa***** klikneme na *****Get device details***** vidíme tam *****device_id:***** do toho vložíme *****Device Name/ID***** ktorý mame okopirovany a stalčime *****Sumbit Request***** ktory je dole, práve nám vyšla odpved v *****Response***** a okopírujeme si iba *****local_key***** a mame hotové, pokiaľ chceme od ďalšieho zariadenia *****local_key***** urobíme to iste len len použijeme iné *****Device Name/ID*****.
### ⚠️Cors funguje iba na Chromium prehlidačoch⚠️

![Cors](https://github.com/DzurisHome/LocalTuyaSK/blob/main/Cors.png)

## 2.2
Pôjdeme na stránku [Node.js](https://nodejs.org/en/download/ "Node.js") a si stiahneme *****Node.js***** a si ho nainštalujeme a po inštalácii si otovorime *****Príkazový Riadok CMD***** a si skopírujeme tam `npm i @tuyapi/cli -g` a dáme enter po ukončení si tam skopírujeme `tuya-cli wizard` a dáme enter po dalšiom ukončení bude to po nás pýtať *****The API key from tuya.com:***** skopírujeme tam svoj *****Access ID/Client ID:***** dáme enter potom *****Access Secret/Client Secret:***** dáme enter bude po nás teraz pýtať *****Provide a 'virtual ID' of a device currently registered in the app:***** vložíme ho tam a dáme zase enter, teraz na nás vyšla *****[odpoveď](https://github.com/DzurisHome/LocalTuyaSK/blob/main/CMD.jpg)***** (Kľúče) teraz si to cele niekde okpirujeme a môžme CMD vypnúť.

![Node JS](https://github.com/DzurisHome/LocalTuyaSK/blob/main/Node%20JS.png)    ![Terminal](https://github.com/DzurisHome/LocalTuyaSK/blob/main/Terminal.png)

## 3
Otvoríme si v *****Home Assistantovi [HACS](https://github.com/hacs)***** klikneme na *****Integrations***** vyhľadáme tam *****[Local Tuya](https://github.com/rospogrigio/localtuya)***** nainštalujeme a dáme reštart Home Assistanta, otvoríme si *****Configuration***** dáme integrations klikneme na *****+ ADD INTEGRATION***** vyhľadáme *****LocalTuya***** klikneme na to vybereme si zariadenie ktoré chceme pridať do *****Home Assistantovi***** dáme *****SUMBIT***** nastavíme Meno, do *****Key:***** pridáme tu odpoveď ktorá nám vyšla vo *****CMD/Tuya*****, rovanko v *****CMD***** je to pomenované ako v *****Home Assostantovi***** a v *****Tuya***** je to *****local_key*****, vybereme najnovší protkol dáme *****SUMBIT***** dalej mame tam *****ID***** nastavíme *****1 (value: False)***** len pokiaľ mame iba *****Switch***** alebo obyčajnú *****Zásuvku***** ktorá nemeria nič, pokiaľ chceme niečo iné pridať tak to spravíme podľa toho to *****[TU](https://github.com/DzurisHome/LocalTuya/blob/main/README.md#32)*****, vidíme *****Friendly name***** tam nastavíme meno akým chceme žeby to dane zariadenie bolo pomenované *****Current***** bude *****1 (value: False)***** tiež tak isto *****Current: Consumption***** aj *****Voltage***** a môžme dať *****SUMBIT***** a hotové.

![Local Tuya](https://github.com/milandzuris/LocalTuyaSK/blob/main/Local%20Tuya.png)    ![Home Assistant](https://github.com/DzurisHome/LocalTuyaSK/blob/main/Home%20Assistant.png)

## 3.2
### [Originál Tutorial 0.1](https://github.com/DrGBHindert/localtuya)
### [Tutorial 0.2](https://github.com/mileperhour/localtuya-homeassistant)
### [Tutorial TinyTuya 0.3](https://pypi.org/project/tinytuya/)

### Zásuvka ktorá nemeria spotrebu ![Potvrdené že to funguje](https://github.com/milandzuris/LocalTuya/blob/main/Verify.png)
```
switch:
  - platform: localtuya
    host: 192.168.0.148 #IP ADRESA
    local_key: fdgdfg45f4g54d5fg4d6f5gdf5gd5f46g #LOCAL KEY
    device_id: dfjngnjdfng445gFGSD54 #DEVICE ID
    protocol: 3.3 #3.3 ALEBO 3.1
    current: Optional
    current_consumption: Optional
    voltage: Optional
    switches:
      Napr. Radiator:
        friendly_name: Radiator #Meno ktoré sa bude ukazovať v HA
        id: 1
   # ©Dzuriš Home
```

### Zásuvka ktorá meria spotrebu ![Potvrdené že to funguje](https://github.com/milandzuris/LocalTuya/blob/main/Verify.png)
```
switch:
  - platform: localtuya
    host: 192.168.0.148 #IP ADRESA
    local_key: fdgdfg45f4g54d5fg4d6f5gdf5gd5f46g #LOCAL KEY
    device_id: dfjngnjdfng445gFGSD54 #DEVICE ID
    protocol: 3.3 #3.3 ALEBO 3.1
    current: 18
    current_consumption: 19
    voltage: 20
    switches:
      Napr. Radiator:
        friendly_name: Radiator #Meno ktoré sa bude ukazovať v HA
        id: 1
   # ©Dzuriš Home
```

### Covers
```
cover:
  - platform: localtuya
    host: 192.168.0.148 #IP ADRESA
    local_key: fdgdfg45f4g54d5fg4d6f5gdf5gd5f46g #LOCAL KEY
    device_id: dfjngnjdfng445gFGSD54 #DEVICE ID
    protocol: 3.3 #3.3 ALEBO 3.1
    open_close_cmds: on_off #on_off ALEBO open_close
    positioning_mode: node #none, position ALEBO fake
    currpos_dps: 3 #Voliteľné, požadované iba pre režim poloha
    setpos_dps: 4 #Voliteľné, požadované iba pre režim poloha
    span_time: 25 #Voliteľné, alebo fake
    covers:
      Napr. Covers:
        friendly_name: Covers #Meno ktoré sa bude ukazovať v HA
        id: 2
   # ©Dzuriš Home
```

### Fan
```
fan:
  - platform: localtuya
    host: 192.168.0.148 #IP ADRESA
    local_key: fdgdfg45f4g54d5fg4d6f5gdf5gd5f46g #LOCAL KEY
    device_id: dfjngnjdfng445gFGSD54 #DEVICE ID
    protocol: 3.3 #3.3 ALEBO 3.1
    fans:
      Napr. Fan:
        friendly_name: Fan #Meno ktoré sa bude ukazovať v HA
        id: 3
   # ©Dzuriš Home
```

### Light
```
light:
  - platform: localtuya
    host: 192.168.0.148 #IP ADRESA
    local_key: fdgdfg45f4g54d5fg4d6f5gdf5gd5f46g #LOCAL KEY
    device_id: dfjngnjdfng445gFGSD54 #DEVICE ID
    protocol: 3.3 #3.3 ALEBO 3.1
    color_mode: 21 #Voliteľné, zvyčajne 2 alebo 21, predvolené: none
    brightness: 22 #Voliteľné, zvyčajne 3 alebo 22, predvolené: none
    color_temp: 23 #Voliteľné, zvyčajne 4 alebo 23, predvolené: none
    color: 24 #Voliteľné, zvyčajne 5 (RGB:HSV) alebo 24 (HSV), predvolené: none
    brightness_lower: 29 #Voliteľné, zvyčajne 0 alebo 29, predvolené: 29
    brightness_upper: 1000 #Voliteľné, zvyčajne 255 alebo 1000, predvolené: 1000
    color_temp_min_kelvin: 2700 #Voliteľné, predvolené: 2700
    color_temp_max_kelvin: 6500 #Voliteľné, predvolené: 6500
    scene: 25 #Voliteľné, zvyčajne 6 (RGB:HSV) alebo 25 (HSV), predvolené: none
    music_mode: False #Voliteľné, niektoré používajú interný mikrofón, iné telefónny mikrofón. Podporovaný je iba interný mikrofón, predvolené nastavenie: False
    lights:
      Napr. Light:
        friendly_name: Light #Meno ktoré sa bude ukazovať v HA
        id: 4 #Zvyčajne 1 alebo 20
   # ©Dzuriš Home
```

### Sensor
```
sensor:
  - platform: localtuya
    host: 192.168.0.148 #IP ADRESA
    local_key: fdgdfg45f4g54d5fg4d6f5gdf5gd5f46g #LOCAL KEY
    device_id: dfjngnjdfng445gFGSD54 #DEVICE ID
    protocol: 3.3 #3.3 ALEBO 3.1
    scaling: 0.1 #Voliteľné
    device_class: voltage #Voliteľné
    unit_of_measurement: "V" #Voliteľné
    sensors:
      Napr. Sensor:
        friendly_name: Sensor #Meno ktoré sa bude ukazovať v HA
        id: 20
   # ©Dzuriš Home
```

### Binary Sensor
```
binary_sensor:
  - platform: localtuya
    host: 192.168.0.148 #IP ADRESA
    local_key: fdgdfg45f4g54d5fg4d6f5gdf5gd5f46g #LOCAL KEY
    device_id: dfjngnjdfng445gFGSD54 #DEVICE ID
    protocol: 3.3 #3.3 ALEBO 3.1
    device_class: power
    state_on: true #Voliteľné
    state_off: false #Voliteľné
    binary_sensors:
      Napr. Binary_Sensor:
        friendly_name: Binary Sensor #Meno ktoré sa bude ukazovať v HA
        id: 1
    # ©Dzuriš Home
```

## Social
[<img src='https://img.icons8.com/nolan/64/discord-logo.png' alt='Discord' height='64'>](https://discord.gg/wpg5aAx) [<img src='https://img.icons8.com/nolan/64/instagram-new.png' alt='Instagram' height='64'>](https://instagram.com/dzurishome) [<img src='https://img.icons8.com/nolan/64/twitter.png' alt='Twitter' height='64'>](https://twitter.com/DzurisHome)

## Social Stats
[![Discord Server](https://discord.com/api/guilds/731017969706205264/embed.png)](https://discord.gg/wpg5aAx) ![Twitter](https://img.shields.io/twitter/follow/DzurisHome?color=00C1FF&style=for-the-badge) ![Discord Server](https://img.shields.io/discord/731017969706205264?style=for-the-badge)

## Repositary Stats
![Issues](https://img.shields.io/github/issues/DzurisHome/LocalTuyaSK?color=FF0000&style=for-the-badge) ![License](https://img.shields.io/github/license/DzurisHome/LocalTuyaSK?style=for-the-badge) ![Forks](https://img.shields.io/github/forks/DzurisHome/LocaltuyaSK?style=for-the-badge) ![Stars](https://img.shields.io/github/stars/DzurisHome/LocalTuyaSK?color=FFE400&style=for-the-badge)  
