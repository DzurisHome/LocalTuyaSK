# Local Tuya Tutorial SK

## [LinkTree](https://linktr.ee/DzurisHome)

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/N4N6M7OX3)

</br>

## Ako integrovať Tuya zariadenia do Home Assistanta cez Local Tuya.

### Výhody
- Funguje to Lokálne nevyužíva Cloud, nie je potreba žiadny Tuya Convert.
- Funguje to aj počas výpadku (ISP) Internetu.

### Podporované Aplikácie
- Tuya
- Smart Life

### Podporované zariadenia
- Switches (Vypínače)
- Lights (Svetla)
- Covers
- Fans
- Climates
- Vacuums (Vysávač)

### Problémy a nedostatky
🚨Pokiaľ sa vyskytne dajaký problém alebo dajaký nedostatok tak to spíš do Issues a ti pomôžem stým.

## Mapa
- [1](https://github.com/DzurisHome/LocalTuya#1) Potrebné bez toho sa ďalej *****neposuvneme*****.
- [2](https://github.com/DzurisHome/LocalTuya#2) Získanie *****KEY/KĽUČA***** cez *****[Tuya IoT](https://iot.tuya.com/)*****.
- [3](https://github.com/DzurisHome/LocalTuya/blob/main/README.md#3) Ako pridať *****Local Tuya***** Integráciu do *****Home Assistanta*****.
- [4](https://github.com/DzurisHome/LocalTuya/blob/main/README.md#4) Ako pridať *****Zariadenie***** do *****Local Tuya*****.
- [5](https://github.com/DzurisHome/LocalTuya/blob/main/README.md#5) Tabuľka *****DP*****
- [6](https://github.com/DzurisHome/LocalTuya/blob/main/README.md#6) Ako zistiť *****DP*****

### 1
Prvé pôjdeme na stránku *****[Tuya IoT](https://iot.tuya.com/)***** tam sa zaregistrujeme a prihlásime potom pôjdeme na položku *****[Cloud](https://iot.tuya.com/cloud/)***** práve vidíme pred sebou na právo *****Create Cloud Project***** klikneme nato potom do *****Project Name***** vložíme dajaký svoj vlastný názov v *****Industry***** dáme *****Smart Home***** v *****Development Method***** zase *****Smart Home***** a v *****Data Center***** najbližší *****Data Center***** a stlačíme dole *****Create***** dalej*****Authorize***** a mame to,
vidíme tam *****Deivces***** klikneme nato potom klikneme na *****Link Tuya App Account***** a ešte klikneme na právo na *****Add App Account***** práve sa nám zobrazil *****QR KOD***** teraz prejdeme do aplikácií čo mame v mobile alebo tablete buď *****(Tuya alebo SmartLife)***** stlačíme to *****plusko***** čo je v právo hore a teraz klikneme Scan a môžme oskenoať ten *****QR KOD***** ktorý sa nám ukázal na *****[Tuya IoT](https://iot.tuya.com/)*****, o skenujeme klineme na *****Confirm login***** potom na *****[Tuya IoT](https://iot.tuya.com/)***** klineme už iba na *****OK***** a prepojenie je úspešne a ešte zatvoríme tu kartu čo nám vyhodilo počas prepojenia Aplikácií.

![Tuya](https://github.com/milandzuris/LocalTuya/blob/main/Tuya.png)

### 2
V *****All Devices***** vyberieme si naše zariadenia ktoré chceme pridať do *****Home Assistant***** a si okopírujeme jeho *****Device ID*****,
teraz prejdeme na *****[Cloud](https://iot.tuya.com/cloud/)***** je na vľavo potom klikneme na *****[API Explorer](https://iot.tuya.com/cloud/explorer)***** nájdeme si tam *****Device Management***** klikneme nato a dáme *****Query Device Details***** vidíme tam *****device_id***** vložíme tam náš *****Device ID***** a stlačíme *****Sumbit Request***** ktorý je dole, práve nám vyšla odpved v *****Response***** skopírujeme si iba *****local_key***** a mame hotové.

![Tuya](https://github.com/DzurisHome/LocalTuyaSK/blob/main/Tuya%20Square.png)

### 3
Otvoríme si v *****Home Assistantovi [HACS](https://github.com/hacs)***** klikneme na *****Integrations***** vyhľadáme tam *****[Local Tuya](https://github.com/rospogrigio/localtuya)***** nainštalujeme a dáme reštart Home Assistanta, otvoríme si *****Configuration***** dáme integrations klikneme na *****+ ADD INTEGRATION***** vyhľadáme *****LocalTuya***** klikneme na to, práve nám vyhodí kartu na vyplnenie, vyplníme *****API server region***** na ten náš ktorý sme zadávali v [1](https://github.com/DzurisHome/LocalTuya#1) a mame na výber buď vyplníme všetky informácie a nemusíme už potom zisťovať pri pridavani nových zariadení *****local_key***** iba *****DP***** alebo za klikneme dole *****Do not configure Cloud API account***** a potom pri každom pridanom zariadení musíme ešte si zistiť *****local_key*****, ak necháme tuto možnosť *****Do not configure Cloud API account***** tak len zaklineme toto a už len *****SUMBIT***** a mame hotovo,
ak vyberieme si možnosť že vyplníme všetko tak *****Clinet ID***** a *****Secret***** všetko sa nachádza ako sme založili náš projekt hneď na začiatku *****[Cloud](https://iot.tuya.com/cloud/)***** a *****User ID***** nájdeme v *****Devices***** potom *****Link Tuya App Account***** a tam mame *****UID***** a to si okopírujeme a pridáme do *****User ID***** a môžme kliknúť na *****SUMBIT***** a mame hotovo.

![Tuya](https://github.com/milandzuris/LocalTuya/blob/main/Tuya.png)

### 4
V *****Integraci***** si nájdeme tam *****Local Tuya***** Integráciu a klineme na ňu a mame tam *****CONFIGURE***** zase nato klineme a je tam hneď *****Add a new device***** toto zanecháme a dáme *****SUMBIT***** a vyberem si ktoré *****Zariadenie***** chceme pridať keď nenašlo tak klikneme na tie bodky a zase dáme *****SUMBIT*****,
vyplníme *****Name***** meno jake chceme *****Host***** IP Adresu *****Device ID***** *****local_key***** ak pridávame sami zariadenie pomocou *****bodiek***** musíme si zistiť aký *****Protocol Version***** a ako pridávame automaticky tak necháme ako to samé nastavilo, *****Scan interval***** nastavíme ak mame produkt ktorý meria spotrebu *****najmenej 5 skeund ak dáme menej môžu byt výpadky a nestabilita zariadenia*****, *****Manual DPS***** si zistime zvyčajne je to *****1*****.

### 5
*****[Tuya Data Points | Dzuriš Home](https://github.com/DzurisHome/Tuya-Data-Points)*****

*****[tuya-uncover | Blakadder](https://github.com/blakadder/tuya-uncover)*****

*****Tabuľka:*****

| Verzia 3.1 (a nejaké 3.3) - Plug alebo Switch |
| DP ID | Funkčný bod | Typ     | Rozsah     | Jednotky     |
|------ | --------------- | -------- | --------- | --------- |
| 1     | Switch          | bool     | True/False|           |
| 4     | Current         | integer  | 0-30000   | mA        |
| 5     | Power           | integer  | 0-50000   | W         |
| 6     | Voltage         | integer  | 0-5000    | V         |

| Verzia 3.1 - Light (RGB) |
| DP ID | Funkčný bod | Typ      | Rozsah                    | Jednotky    |
|------ | --------------- | --------- | ------------------------ | -------- |
| 1     | Switch          | bool      | True/False               |          |
| 2     | Mode            | enum      | white, colour, scene, music|         |
| 3     | Bright          | integer   | 10-1000*                 |          |
| 4     | Color Temp      | integer   | 0-1000*                  |          |
| 5     | Color           | hexstring | r:0-255, g:0-255, b:0-255, h:0-360, s:0-255, v:0-255 | rgb+hsv |

| Verzia 3.3 - Plug, Switch, Power Strip |
| DP ID | Funkčný bod | Typ     | Rozsah     | Jednotky     |
|------ | --------------- | -------- | --------- | --------- |
| 1     | Switch 1        | bool     | True/False|           |
| 2     | Switch 2        | bool     | True/False|           |
| 3     | Switch 3        | bool     | True/False|           |
| 4     | Switch 4        | bool     | True/False|           |
| 5     | Switch 5        | bool     | True/False|           |
| 6     | Switch 6        | bool     | True/False|           |
| 7     | Switch 7/usb    | bool     | True/False|           |
| 18    | Current         | integer  | 0-30000   | mA        |
| 19    | Power           | integer  | 0-50000   | W         |
| 20    | Voltage         | integer  | 0-5000    | V         |

| Verzia 3.3 - Dimmer Switch |
| DP ID | Funkčný bod | Typ     | Rozsah     | Jednotky     |
|------ | --------------- | -------- | --------- | --------- |
| 1     | Switch          | bool     | True/False|           |
| 2     | Brightness      | integer  | 10-1000* |           |
| 3     | Minimum of Brightness | integer | 10-1000* |       |
| 4     | Type of light source1 | enum | LED, incandescent, halogen | |
| 5     | Mode            | enum     | white     |           |

| Verzia 3.3 - Light (RGB) |
| DP ID | Funkčný bod | Typ     | Rozsah     | Jednotky     |
|------ | --------------- | -------- | --------- | --------- |
| 20    | Switch          | bool     | True/False|           |
| 21    | Mode            | enum     | white, colour, scene, music | |
| 22    | Bright          | integer  | 10-1000* |           |
| 23    | Color Temp      | integer  | 0-1000   |           |
| 24    | Color           | hexstring | h:0-360, s:0-1000, v:0-1000 | hsv |
| 25    | Scene           | string   | n/a       |           |
| 26    | Left time       | integer  | 0-86400  | s         |
| 27    | Music           | string   | n/a       |           |

| Verzia 3.3 - Automated Curtain |
| DP ID | Funkčný bod         | Typ    | Rozsah          | Jednotky |
|------ | ---------------------- | ------- | --------------- | ----- |
| 1     | Curtain Switch 1      | enum    | open, stop, close, continue | |
| 2     | Percent control 1     | integer | 0-100           | %     |
| 3     | Accurate Calibration 1 | enum    | start, end      |       |
| 4     | Curtain Switch 2      | enum    | open, stop, close, continue | |
| 5     | Percent control 2     | integer | 0-100           | %     |
| 6     | Accurate Calibration 2 | enum    | start, end      |       |
| 8     | Motor Steer 1         | enum    | forward, back   |       |
| 9     | Motor steer 2         | enum    | forward, back   |       |
| 10    | Quick Calibration 1    | integer | 1-180           | s     |
| 11    | Quick Calibration 2    | integer | 1-180           | s     |
| 12    | Motor Mode 1          | enum    | strong_power, dry_contact | |
| 13    | Motor Mode 2          | enum    | strong_power, dry_contact | |
| 14    | Light mode            | enum    | relay, pos, none |       |

| Verzia 3.3 - Fan Switch |
| DP ID | Funkčný bod        | Typ    | Rozsah        | Jednotky |
|------ | --------------------- | ------- | -----------   | ----- |
| 1     | Fan switch            | bool    | True/False   | n/a   |
| 2     | Fan countdown         | integer | 0-86400      | s     |
| 3     | Fan speed             | enum    | level_1, level_2, level_3, level_4, level_5 | |
| 4     | Fan speed             | integer | 1-100        | %     |
| 5     | Fan light switch      | bool    | True/False   |       |
| 6     | Brightness            | integer | 10-1000      |       |
| 7     | Fan light countdown    | integer | 0-86400      | s     |
| 8     | Minimum brightness    | integer | 10-1000      |       |
| 9     | Maximum brightness    | integer | 10-1000      |       |
| 10    | Mode                  | enum    | white        |       |
| 11    | Power-on state setting | enum    | off, on, memory |     |
| 12    | Indicator status setting | enum  | none, relay, pos |       |
| 13    | Backlight switch      | bool    | True/False   |       |

![Local Tuya](https://github.com/milandzuris/LocalTuyaSK/blob/main/Local%20Tuya.png)    ![Home Assistant](https://github.com/DzurisHome/LocalTuyaSK/blob/main/Home%20Assistant.png)

</br>

## [LinkTree](https://linktr.ee/DzurisHome)

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/N4N6M7OX3)
