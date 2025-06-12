-----

|Dokumentum információk|Col2|
|---|---|
|Projekt neve|HRP SZEM|
|Projekt kódja||
|Megrendelő neve|MÁV Zrt.|
|Dokumentum címe|Műszaki specifikáció|
|Verziószám|1.0|


|Dokumentumtörténet|Col2|Col3|Col4|
|---|---|---|---|
|Verzió|Dátum|Szerkesztette|Leírás|
|1.0|2025.01.02.|Turóczi Márton||
|||||
|||||
|||||
|||||
|||||
|||||
|||||


**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

### **Tartalom **

1 Áttekintés ........................................................................................................................................ 5

A dokumentum célja .................................................................................................................................... 5

2 Folyamat modell – Üzleti folyamatok .............................................................................................. 6

3 Követelménymodell ......................................................................................................................... 8

4 Ablakfolyam diagram ....................................................................................................................... 8

5 Funkcionális és felület modell – Üzleti funkciók és képernyők bemutatása ................................... 9

Szerepkörök .................................................................................................................................................. 9

Fogalmak ...................................................................................................................................................... 9

Státuszok ...................................................................................................................................................... 9

Szemüveg igénylése képernyő ................................................................................................................... 10

Partnertörzs rögzítés képernyő .................................................................................................................. 11

Könyvelés képernyő ................................................................................................................................... 12

Riportok képernyő ...................................................................................................................................... 12

5.7.1 Bérszámfejtési riport képernyő ..................................................................................... 12

5.7.2 Munkabaleset form .......................................................... **Error! Bookmark not defined.**

Személyes és munkahelyi adatok (form bal oldala) ......................................... **Error! Bookmark not defined.**
Munkabaleset adatai (form jobb oldala) .......................................................... **Error! Bookmark not defined.**
Fogalommagyarázat ...................................................................................... **Error! Bookmark not defined.**

Szabályok ....................................................................................................... **Error! Bookmark not defined.**

Szerepkörök, jogosultságok ........................................................................... **Error! Bookmark not defined.**

A rendszer működésének folyamata ............................................................. **Error! Bookmark not defined.**

Funkcionális és felület modell – Üzleti funkciók és képernyők bemutatása . **Error! Bookmark not defined.**

5.12.1 Ablakfolyam diagram ........................................................ **Error! Bookmark not defined.**

5.12.2 Kódszótárak ...................................................................... **Error! Bookmark not defined.**

Vállalat adatai kódszótár működése................................................................. **Error! Bookmark not defined.**

Szervezeti egységek (Volánbusz) kódszótár működése ................................... **Error! Bookmark not defined.**
Telephely (Volánbusz) kódszótár működése ................................................... **Error! Bookmark not defined.**
FEOR kódok (Volánbusz) kódszótár működése .............................................. **Error! Bookmark not defined.**
Képzettséget igazoló irat száma kódszótár működése ..................................... **Error! Bookmark not defined.**

Vállalati terület kódszótár működése ............................................................... **Error! Bookmark not defined.**

Szakterület kódszótár működése ...................................................................... **Error! Bookmark not defined.**
Fő tevékenységi kör (TEÁOR kódok) kódszótár működése ............................ **Error! Bookmark not defined.**
5.12.3 A munkabaleset képernyő ................................................ **Error! Bookmark not defined.**

A munkabaleset rögzítése form működése ...................................................... **Error! Bookmark not defined.**

5.12.4 E-mail sablonok .............................................................................................................. 16

Automatikusan küldött e-mailek ...................................................................... **Error! Bookmark not defined.**

Manuálisan küldött e-mailek ........................................................................... **Error! Bookmark not defined.**

Adatbázis tervezet – Fizikai adatmodell ..................................................................................................... 19

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

5.13.1 Tábla 1 .............................................................................. **Error! Bookmark not defined.**

5.13.2 Tábla 2 .............................................................................. **Error! Bookmark not defined.**

Tárolt eljárások .............................................................................................. **Error! Bookmark not defined.**

5.14.1 Eljárás 1 ............................................................................. **Error! Bookmark not defined.**

5.14.2 Eljárás 2 ............................................................................. **Error! Bookmark not defined.**

Rendszerkapcsolatok .................................................................................................................................. 20

5.15.1 Interfész 1 ......................................................................... **Error! Bookmark not defined.**

Átadandó állomány formátuma, névkonvenció ............................................... **Error! Bookmark not defined.**
Átadandó állomány struktúrája ........................................................................ **Error! Bookmark not defined.**
Előállítás módja, ütemezés, paraméterezés ...................................................... **Error! Bookmark not defined.**
Átadás módja, helye, hibakezelés .................................................................... **Error! Bookmark not defined.**
Logikai adatmapping ....................................................................................... **Error! Bookmark not defined.**
6 Érintettség vizsgálat ....................................................................................................................... 21

Érintett szerver oldali változások .................................................................. **Error! Bookmark not defined.**

Érintett rendszerkapcsolatok ..................................................................................................................... 21

Érintett HÖP modulok ................................................................................................................................ 21

Dokumentum érintettség ........................................................................................................................... 21

6.4.1 Másik modul rendszertervének érintettsége ................... **Error! Bookmark not defined.**

6.4.2 HÖP felhasználói kézikönyv érintettsége ...................................................................... 21

6.4.3 HÖP üzemeltetési kézikönyv érintett ............................... **Error! Bookmark not defined.**

6.4.4 IMFT érintett .................................................................................................................. 21

6.4.5 RIBSZ érintett .................................................................... **Error! Bookmark not defined.**

7 Mellékletek ....................................................................................... **Error! Bookmark not defined.**

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

### 1 Áttekintés

A MÁV Zrt. mint Megrendelő, felkérte a MÁV Szolgáltató Központ Zrt.-t, hogy adjon ajánlatot az Éleslátást biztosító
szemüveg költségtérítés igénylése (továbbiakban: **SZEM** ) HRP-ben történő kezelésére vonatkozóan.

A HR Portál fejlesztése az Oriana (Effector) platformon történik.
##### A dokumentum célja

A dokumentum célja ismertetni a MÁV- csoport **SZEM projekttel** szemben támasztott követelmények alapján
fejlesztésre kerülő rendszer műszaki specifikációját.

A dokumentumban vázolt megoldási javaslat a rendszer áttekintését tartalmazza. A megvalósítási javaslat a MÁV
SZK által elkészítendő elemekre terjed ki részletesen. A rendszer működéséhez harmadik fél által biztosított elemek
csak a szükséges kapcsolódás szintjén szerepelnek, feltárva a működésre gyakorolt kritikus hatásukat.

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

### 2 Folyamat modell – Üzleti folyamatok

A SZEM modul lehetőséget ad az igénylési folyamat egy felületen történő kezelésére, továbbá az adatok központi,
biztonságos tárolására, így az igénylés egységes és hatékony kezelését segíti elő.
A folyamat az alábbi ábrán látható:

Az üzleti folyamat:

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

A technikai folyamat:

A munkavállaló, aki jogosult éleslátást biztosító szemüveg költségtérítésre belép a HR Portál rendszerbe. A
SZEMÜVEG KÖLTSÉGTÉRÍTÉS modul csak azoknak a munkavállalóknak elérhető, akik olyan munkakörben
dolgoznak, ami a megadott adatok alapján jogosulttá teszi őket a szemüveg költségtérítésre. Ehhez fel kell tölteniük
egy megfelelő számla képet (digitális számla, vagy papír alapú szkennelt változata), valamint a MÁV
Vasútegészségügy Nonprofit Kft által kiállított üzemorvosi (szemészeti) igazolást a szemüveg szükségességéről.

A számla maximum 35.000 Ft összegű lehet (0, vagy kisebb érték sem lehet).

A két dokumentum feltöltését követően az igénylő felhasználó kitölti a formot a számláról leolvasható adatokkal.
Ha a számlát kiállító cég (optika) szerepel a partnertörzsben, az igénylő kiválasztja, ellenkező esetben a mező
kitöltése nélkül menti az űrlapot. A rendszer a Partnertörzs rögzítő jogosultságú felhasználó számára a "Partnertörzs
rögzítés" képernyőn létrehozza a rögzítés feladatát.

Ha a Partnertörzs rögzítő jogosultságú felhasználó nem tudja megállapítani az Optika (Szállító) nevét, akkor vissza
tudja küldeni a  gombbal. Ilyenkor kötelező megjegyzést szükséges megadni.

Ha meg tudja állapítani az Optika (szállító) nevét, akkor a Partnertörzs rögzítő az SAP FI moduljában rögzíti
partnerként a céget (optikát). Ezt követően a partnertörzs interfészen keresztül rövidesen automatikusan frissül a
lista, majd az újonnan felvett érték kiválasztható lesz.

Az újonnan felvett optikát (partnert) a partnertörzs rögzítő pótolja a költségtérítés igényen.

A form ellenőrzése után a "Mentés és tovább (jóváhagyásra)" gombra kattintva lehet véglegesíteni és tovább
küldeni jóváhagyásra. Ekkor átkerül a számlakép az SAP CRM-be, ahonnan a CRM azonosító automatikusan
visszaadásra kerül a HR Portál számára. A CRM-ben az igény vagy jóváhagyásra, vagy elutasításra, vagy pedig
hiánypótlásra visszaküldésre kerül, mely információ szintén interfészen keresztül átadásra kerül a HR Portál felé.

Jóváhagyás esetén a könyvelő tudja ellenőrizni a könyvelendő adatokat a HR Portál felületén. (Adatok
ellenőrzésének hely és az adatok köre a 6.3-as fejezetben kerül kifejtésre)

Ha Elutasításra kerül, a folyamat véget ér, az elutasított státusz látszik a HR Portál felületén.

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

Amennyiben vissza lett küldve hiánypótlásra, akkor az igénylő munkavállaló tudja módosítani a visszaküldő
megjegyzése alapján, majd újra tovább küldeni az SAP CRM felé jóváhagyásra.

Amennyiben jóváhagyás történt, a könyvelő leellenőrzi a számla adatokat (és a számlaképet), és könyvelésre feladja

az adott számlát.

Ezt a "Könyvelés" képernyőn látja. Itt lehetősége van a számla adatainak módosítására, a könyvelésnek (SAP FI)

feladás előtt.
### 3 Követelménymodell

A SZEM modul kialakításának legfontosabb céljai

- Az éleslátást biztosító szemüveg költségtérítés igénylése HR Portálba történő integrálása lehetővé teszi a
folyamat nyomon követhetőségét, átláthatóságát.

- Adminisztratív terhek csökkentése, a folyamat egyszerűbbé, gyorsabbá tétele

- A folyamatban részt vevők (Munkavállalók, Könyvelők, Partnertörzs rögzítésre kijelölt munkatársak)
munkájának támogatása

- Interfésszel automatikus feladás az SAP CRM és az SAP FI felé (jóváhagyásra, illetve könyvelésre).
### 4 Ablakfolyam diagram

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

##### Szere p körök





|Szerepkör|Betöltő munkavállaló|Feladat és jogosultság|
|---|---|---|
|IT adminisztrátor|MÁV SZK IT üzletág üzemeltetés HRP alkalmazás megoldócsoport|HRP rendszer informatikai menedzselését végzi, felhasználókat támogatja a rendszer használatában. Jogosultsága a teljes HRP rendszerre kiterjed.|
|HRP adminisztrátor|Cégcsoport szinten egy munkavállaló|HRP kódszótárak értékek, valamint levélsablonok karbantartása. Jogosultsága csak a kódszótárakra és levélsablonokra terjed ki.|
|Igénylő munkavállaló|Szemüveg igénylésre jogosult munkakörben dolgozó munkavállaló|A szemüveg igénylését elindítja, a folyamatot tudja követni|
|Partnertörzs rögzítő|Szakterület kijelölt munkatársa|Partnertörzs rögzítése a feladata, valamint a partner kiválasztása,|
|||miután frissült a lista a HR Portál felületén.|
|Könyvelő|Szakterület kijelölt munkatársa|Könyveléshez adatok ellenőrzése, szerkesztése, könyvelésre feladás|


A jogosultságokat a MÁV SZK HelpDesknek kell bejelenteni az érintett munkavállaló munkáltatói jogkörgyakorló
egyetértésével. Bejelentés után a HelpDesk adja meg a jogosultságokat a HRP-ban.
##### Fogalmak

SZEM: Éleslátást biztosító szemüveg költségtérítés igénylése

HRP: HR Portál
##### Státuszok

|Státusz neve|Col2|szín|Leírás|
|---|---|---|---|
|Tervezett|100|sárga|Igénylés szerkesztés alatt, elküldés előtt|
|Hiánypótlásra vár|105|piros|Partnertörzs rögzítőtől visszaküldés esetén|
|Partnertörzsre vár|110|kék|Partnertörzs rögzítés folyamatban|
|Jóváhagyásra küldve|120|kék|Jóváhagyásra elküldve SAP CRM felé|
|CRM befogadta|125|kék|SAP CRM befogadta (első hívásnál megérkezik a CRM azonosító az aszinkron interfészen keresztül)|



**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*



-----

|Jóváhagyás visszaküldés (hiánypótlás)|150|piros|SAP CRM felől hiánypótlásra visszaküldve|
|---|---|---|---|
|Jóváhagyás elfogadva (könyvelés)|130|zöld|SAP CRM felől jóváhagyva, könyvelési feladat folyamatban|
|Könyvelésre feladva|160|zöld|SAP FI felé elküldve könyvelésre|
|Könyvelési hiba|165|szürke|Könyvelésre feladás során az SAP FI felől hibaüzenet érkezett|
|Lezárva|200|szürke|Könyvelésre feladást az SAP FI sikeresen feldolgozta, a folyamat vége|
|Jóváhagyás elutasítva|210|szürke|SAP CRM felől az igény elutasítva, a folyamat vége|

##### Szemüveg igénylése képernyő

Az igénylést a jogosult munkavállaló tudja elindítani.

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

A képernyőn látja a saját igényléseit, itt tud új igénylést elindítani, illetve a folyamatban lévő igénylést megtekinteni
(adott esetben módosítani). Új szemüveg igénylés akkor jöhet létre, ha az adott naptári éven belül nem volt sikeres
igénylése.

  - Szemüveg igénylés kártyák

`o` Egy kijelölhető
`o` A kártyán látható adatok:

         - Egyedi azonosító (a címsorban)

         - Igénylő munkavállaló neve

         - Igénylés időpontja

         - Státusz (vízjel)

  - Szűrőmezők

`o` Vállalat

`o` Név (törzsszám)
`o` Egyedi azonosító
`o` Év

`o` Igénylés dátuma

`o` Státusz
##### Partnertörzs rögzítés képernyő

A Partnertörzs rögzítés képernyő a Partnertörzsre vár státuszú kártyák jelennek meg. Csak a Partnertörzs rögzítő és
a SZEM Admin jogosultsággal rendelkező felhasználók látják ezt a képernyőt. Alapértelmezett szűrés: év szűrő az
aktuális év szűrésével (módosítható).

  - Szemüveg igénylés kártyák

`o` Egy kijelölhető
`o` A kártyán látható adatok:

         - Egyedi azonosító (a címsorban)

         - Igénylő munkavállaló neve

         - Igénylés időpontja

         - Státusz (vízjel)

  - Szűrőmezők

`o` Vállalat

`o` Név (törzsszám)
`o` Egyedi azonosító

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

`o` Év

`o` Igénylés dátuma
##### Könyvelés képernyő

Ezen a képernyőn azok a kártyák jelennek meg, amelyek a jóváhagyásra kerültek (Jóváhagyás: elfogadva
státuszúak). Alapértelmezett szűrő: Év (aktuális év – változtatható).

  - Szemüveg igénylések táblázatos nézetben

`o` Egy kijelölhető
`o` A táblázatos nézet oszlopai:

         - Egyedi azonosító

         - Név (törzsszám)

         - Vállalat

         - Szállító

         - Adószám

         - Számla sorszáma

         - Igénylés dátuma

         - Számla kelte

         - Bruttó összeg (Ft)

         - Áfa mértéke

         - Könyvelési dátum a bizonylaton

         - Státusz

  - Szűrőmezők

`o` Vállalat

`o` Név (törzsszám)
`o` Egyedi azonosító
`o` Év

`o` Igénylés dátuma

`o` Státusz

`o` Aktív adatok (jelölőnégyzet)
##### Riportok képernyő 5.7.1 Bérszámfejtési riport képernyő

A lezárt (könyvelésre sikeresen feladott) kártyák jelennek meg. Alapértelmezett szűrő: Év (aktuális naptári év változtatható).

  - Szemüveg igénylések táblázatos nézetben

`o` Egy kijelölhető
`o` A táblázatos nézet oszlopai:

         - Egyedi azonosító

         - Név (törzsszám)

         - Vállalat

         - Szállító

         - Adószám

         - Számla sorszáma

         - Igénylés dátuma

         - Számla kelte

         - Bruttó összeg (Ft)

         - Áfa mértéke

         - Könyvelési dátum a bizonylaton

  - Szűrőmezők

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

`o` Vállalat

`o` Név (törzsszám)
`o` Egyedi azonosító
`o` Év

`o` Igénylés dátuma
`o` Aktív adatok (jelölőnégyzet)
##### Szemüveg igénylés űrlap (form)

Új igénylés indításakor, vagy meglévő megtekintésekor a következő form jelenik meg a felhasználónak:

Szerkeszthető mezők:

  - Üzemorvosi igazolás (fájl csatolása)

  - Számla (fájl csatolása)

  - Számla sorszáma

  - Számla kelte

  - Szállító kódja: a partnertörzsből kiválasztható.

  - Számla bruttó összege (Ft-ban): maximum 35.000 Ft lehet

  - ÁFA mértéke (kiválasztható): 27% vagy 0%

Jobb oldalon megjelenik a feltöltött számlakép, és egy másik fülön az üzemorvosi igazolás.

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

**Hibakezelés/Rendszerüzenetek**

Az adott képernyőhöz tartozó rendszerüzenetek:



|Esetleírás (HA)|Hibaüzenet (AKKOR)|Jelzés típusa|Futás befolyásolás|
|---|---|---|---|
|Kötelező mező üres|A (…) mező kitöltése kötelező!|Hiba|Nem történik mentés|
|Számla értéke nem megfelelő|A számla bruttó összege 1 és 35.000 között kell legyen!|Hiba|Nem történik mentés|


A partner kiválasztása külön ablakban tud történni (általános keresőmező minden mezőben keres):

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

A **partnertörzs rögzítő** azokat az igényléseket látja, amelyekkel feladata van. Itt egyetlen mezőt tud módosítani, a
szállító kódját:

A **könyvelő** számára több mező szerkeszthető, de a feltöltött fájlokon már nem tud módosítani.

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

##### 5.8.1 E-mail sablonok – automatikus értesítések

*Ügyfélszolgálat az igényt jóváhagyja*

Itt a cél csupán a tájékoztatás, munkavállalónak csak tudomásul kell vennie.

Kedves %Munkavállaló neve%!

A HRP Szemüveg költségtérítés modulban a %iktatószám% ügyszámon feladott elszámolási igénye jóváhagyásra

került.

Igény részletei:

Igénylő neve: %igénylő munkavállaló neve%

Törzsszám: %igénylő munkavállaló törzsszáma%

Link a HRP szemüveg költségtérítés oldal adott feladatkártyájára (Szemüveg költségtérítés/Szemüveg igénylése
képernyőn)

Ez egy automatikus e-mail, kérjük ne válaszoljon rá!

*Ügyfélszolgálat, vagy Partnertörzs rögzítő hiánypótlást kér*

Ebben az esetben a munkavállalónak teendője van, amit az Ügyfélszolgálat munkatársa CRM jegyzetben, vagy
Partnertörzs rögzítő üzenetben konkrétan leír.

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

Kedves %Munkavállaló neve%!

A HRP Szemüveg költségtérítés modulban a %iktatószám% ügyszámon feladott elszámolási igényének elbírálásához
hiánypótlás szükséges.

Igény részletei:

Igénylő neve: %igénylő munkavállaló neve%

Törzsszám: %igénylő munkavállaló törzsszáma%

Hiánypótlás tárgya:

%Ügyfélszolgálati referens által a CRM jegyzetbe, vagy Partnertörzs rögzítő által üzenetben beírt szöveg

átemelése%

Link a HRP szemüveg költségtérítés oldal adott feladatkártyájára mutasson, konkrétan oda, ahol fel kell töltenie a
hiánypótlásban érintett dokumetumot (Szemüveg költségtérítés/Szemüveg igénylése képernyőn)

Ez egy automatikus e-mail, kérjük ne válaszoljon rá!

*Ügyfélszolgálat az igényt elutasítja*

Ebben az esetben a munkavállalónak feladata nincs, de az elutasítás okát az Ügyfélszolgálat munkatársa CRM
jegyzetben konkrétan leírja.

Kedves %Munkavállaló neve%!

A HRP Szemüveg költségtérítés modulban a %iktatószám% ügyszámon feladott elszámolási igénye elutasításra

került.

Igény részletei:

Igénylő neve: %igénylő munkavállaló neve%

Törzsszám: %igénylő munkavállaló törzsszáma%

Elutasítás indoklása:

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

%Ügyfélszolgálati referens által a CRM jegyzetbe beírt szöveg átemelése%

Link a HRP szemüveg költségtérítés oldal adott feladatkártyájára mutasson (Szemüveg költségtérítés/Szemüveg
igénylése képernyőn)

Ez egy automatikus e-mail, kérjük ne válaszoljon rá!

*Partnertörzs: mikor partnertörzs rögzítőhöz érkezik a partnertörzs rögzítés feladata*

Címzett: MVZ-Partnertörzs (partnertorzs@mav.hu)

Tárgy: HRP %iktatószám% partnertörzs feladat

Tisztelt Partnertörzskezelő csoport!

A HRP Szemüveg költségtérítés modulban a %iktatószám% ügyszámon partnertörzskezelői feladat keletkezett.

Igény részletei:

Igénylő neve: %igénylő munkavállaló neve%

Törzsszám: %igénylő munkavállaló törzsszáma%

Link a HRP szemüveg költségtérítés oldal adott feladatkártyájára (Szemüveg költségtérítés/Partnertörzs rögzítés
képernyőn)

Ez egy automatikus e-mail, kérjük ne válaszoljon rá!

*Bejövő számla könyvelő: mikor CRM-ben jóváhagyják az igényt*

Címzett: MÁV-SZK könyvelés (konyveles@mav-szk.hu)

Tárgy: HRP %iktatószám% könyvelő feladat

Tisztelt Bejövő számla könyvelés!

A HRP Szemüveg költségtérítés modulban a %iktatószám% ügyszámon feladott elszámolási igény a Humán
szolgáltatás részéről jóváhagyásra került. Kérjük ellenőrizze a számla alapján a rögzített adatokat.

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

Igény részletei:

Igénylő neve: %igénylő munkavállaló neve%

Törzsszám: %igénylő munkavállaló törzsszáma%

Link a HRP szemüveg költségtérítés oldal adott feladatkártyájára (Szemüveg költségtérítés/Könyvelés képernyőn)

Ez egy automatikus e-mail, kérjük ne válaszoljon rá!

*Bejövő számla könyvelő: mikor könyvelésre feladás I0055 interfészen hibára fut (hibaüzenet az*
*üzenetek közé íródik)*

Címzett: MÁV-SZK könyvelés (konyveles@mav-szk.hu)

Tárgy: HRP %iktatószám% könyvelésre feladása során hiba történt

Tisztelt Bejövő számla könyvelés!

A HRP Szemüveg költségtérítés modulban a %iktatószám% ügyszámon feladott elszámolási igény interfészen
történő könyvelésre feladása során hiba történt.

Igény részletei:

Igénylő neve: %igénylő munkavállaló neve%

Törzsszám: %igénylő munkavállaló törzsszáma%

Könyvelésre feladás során kapott hibaüzenet:

%hibaüzenet%

Link a HRP szemüveg költségtérítés oldal adott feladatkártyájára (Szemüveg költségtérítés/Könyvelés képernyőn)

Ez egy automatikus e-mail, kérjük ne válaszoljon rá!
##### Adatbázis tervezet – Fizikai adatmodell

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

##### Rendszerkapcsolatok Interfészek

- HRP Törzsadat interfész

`o` Munkavállalók adatai

`o` Modul láthatósága csak a képernyő előtti munkavégzésben érintett felhasználóknak

- Partnertörzs interfész (Partnertörzs rögzítés eredménye)

`o` Partnertörzs berögzítése után jön át az adat, ez alapján az új partner is a listából kiválasztható lesz

- CRM interfész (aszinkron)

`o` Jóváhagyásra küldés (első alkalommal)

`o` Automatikusan visszaérkezik a CRM azonosító

`o` A két fájl elküldésre kerül SAP CRM felé, ahol döntenek a jóváhagyásról
`o` Döntés eredménye visszajön az interfészen keresztül (Engedélyezés, Elutasítás vagy Visszaküldés

hiánypótlásra)

- CRM update (hiánypótlás utáni küldésnél)

`o` Második, vagy további küldésnél

`o` Szinkron hívás - azonnal érkezik a válasz

- Könyvelés interfész (SAP FI)

`o` Könyvelésre feladás SAP FI felé
`o` Automatikus válasz érkezik (rendben/hiba)

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

### 6 Érintettség vizsgálat
##### Érintett rendszerkapcsolatok Érintett HÖP modulok Dokumentum érintettség 6.3.1 HÖP felhasználói kézikönyv érintettsége

Az Effector Platformon működő HR Portál általános felhasználói kézikönyve változatlan a korábbi dokumentumban

leírt működtetéssel.

A modulhoz felhasználói kézikönyv készült.
##### 6.3.2 IMFT érintett

Az IMFT dokumentum legutolsó verziója a modul működésének is megfelelő.

**MÁV Szolgáltató Központ Zrt. IT Üzletág**
*1087 Budapest, Könyves Kálmán krt. 54-60. Tel.: +36-1 457-9300; fax: +36-1 457-9500; e-mail: it@mav-szk.hu*


-----

