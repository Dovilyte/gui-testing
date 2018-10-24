## When to Automate User Stories

https://www.testingexcellence.com/when-should-stories-be-automated/
1. Automatiniai testai turėtų būti pakartojami. 
2. Patikimumas. (Automatiniai testai turėtų pereit patikras)
3. Laikas. Automatiniai testai turėtų sutaupyti laiką. (Jei greičiau rankiniu būdu atlikti, tada naudoti jį )
4. Apsaugoti developerius. (Automatizuoti testai turėtų apdrausti programerius, o pasikeitus kodo bazei, būtų greitai pranešta programuotojams.)
5. Kada user stories turėtų būti automatizuotos? 
Bottom line yra - bet koks bandymas, kuris bus atliekamas daugiau nei vieną kartą.
pvz. Reggresion tests - Testai, pagal kuriuos nustatoma, ar programa pritaikius naujus pakeitimus ir funkcijas.
Geriausias automatinio testavimo tikslas yra regresijos testavimas ir regresijos testai visada vykdomi atsižvelgiant į žinomą būklę ir deterministinę sistemą, kad būtų galima nustatyti bazinės linijos pokyčius ir gauti reikšmingą rezultatą automatizuotame bandyme, yra tik tada, kai bandymas vykdomas ir bent kartą perduodama rankiniu būdu, kad galėtumėte palyginti automatizuoto paleidimo rezultatus su rankiniu būdu atliktu veiksmu.
Istorijos turėtų būti automatizuotos (įgyvendinimas) per sprintą ir tik tada, kai funkcija yra visiškai patikrinta rankiniu būdu.
*Galima dar susijusių straisnių paskaityt iš šitos nuorodos nukreipia.

## Automated GUI Testing: How to Get It Right
https://testlio.com/blog/how-to-automate-gui-testing/
1. Automatinis testas yra kritinis.
Norint išsiaiškinti sudėtingesnes problemas. 
Pagalba apima galiojančių funcijų kokybę.
Suteikti nuolatinį, pastovų atsiliepimą apie kokybę ir našumą. 
Vienas iš sudėtingaiusių bet kokios programinės įrangos automatizavimo aspektų yra grafinės vartotojo sąsajos GUI testavimas.
1. Pašalinkite sistemos funkcionaumą iš GUI testavimo.
Pirmiausia pašalinkite viską iš GUI testavimo, kuris iš tikrųjų nėra GUI testavimas.
Dauguma sistemos kritinio funkcionalumo gali būti visiškai atskirtos nuo GUI. 
Bet kuris automatinis testas, kurio scenarijus nurodo laukų pavadinimus ir mygtukus, gali būti perrašytas, kai šie laukai ir mygtukai pervadinami.
2. Naudokite abstrakcijas. 
Abstrakcijos naudojimas yra dar vienas būdas palengvinti GUI testavimo automatizavimo rinkinį. Abstrakcija užima tam tikrą informaciją apie tai, kaip bandymas atliekamas. Tai rekonstrukcijos forma, kurioje jūs keičiate kodą, kad jį patobulintumėte nekeisdami elgesio.
3. Mokintis iš rankinio testavimo. 
Automatinis testavimas toli gražu nekeičia rankinio testavimo, o jo tikrinimas ir kūrimas iš tikrųjų reikalauja produkto rankinio testavimo. Kiekvieno rankinio testo pagrindu sudaro trys komponentai:

- Užduotis, kurią reikia atlikti.
- Susiję duomenys, reikalingi užduočiai atlikti.
- Tikėtinas rezultatas.
4. Rankinis testavimas tikrina, ar jis yra tinkamoje produkto srityje, nusprendžia, kaip atlikti užduotį, užtikrina, kad aplinka ir kontekstas yra vietoje, ir tikrina laukiamą rezultatą.
5. Pasitikėkite tinkamais įrankiais. 
6. Norint padidinti investicijų grąžą, labai svarbu pasirinkti tinkamas automatizavimo priemones. Bet koks automatizavimo projektas turėtų būti vertinamas kaip programinės įrangos kūrimo projektas, ty jis bus nuolat kartojamas. Automatika yra aktyvus, nuolatinis procesas. Taigi, jūs norėsite pasirinkti automatikos komplektą, kuris dirbs su savimi ir jūsų komanda.

Automatinio testavimo privalumai:

- Lengva išmokti.
- Paprasta komanda. 

Įrašymas: norint automatiškai rašyti testavimo scenarijus, jūs turėsite pasirinkti GUI testavimo įrankį.
Integracija - didžiausias testų automatizavimo iššūkis.
Automatiniai GUI testai gali užtikrinti nuolatinį grįžtamąjį ryšį apie vartotojo aplinką, efektyvumo ir funkcionalumo patikrinimą bei kartojamų bandymų rezultatų palyginimą.

## How to Set Up Your Automated Functional GUI Tests with Selenium WebDriver
https://www.blazemeter.com/blog/how-to-set-up-your-automated-functional-gui-tests-with-selenium-webdriver
Geras GUI (grafinis vartotojo sąsaja) automatizuotas bandymas imituoja rankinio testavimo veiksmus. Tokiu bandymu automatinis bandymas sąveikauja su mygtukais, teksto laukais ir kitais elementais taip pat, kaip ir rankinis naudotojas, kad galėtumėte sekti tikruoju scenarijumi.
Jūsų aplinkos konfigūravimas. 
1. Įdiekite savo mėgstamą IDE.
Pasirinkite savo mėgstamą IDE (mano yra IntelliJ IDEA) kodo rašymui.
2. Sukurkite naują Maven / Gradle projektą.
3. Atsisiųskite teisingą "WebDriver".
(Populiariausios naršyklės yra "Chrome" ir "Firefox", kurių "WebDrivers" yra atitinkamai "ChromeDriver" ir "geckodriver".)
4. Nustatykite sistemos nuosavybę.
5. Atsisiųskite "Selenium WebDriver".
6.  Pridėkite priklausomybes. example:

```xml
<dependency>
<groupId>org.seleniumhq.selenium</groupId>
<artifactId>selenium-java</artifactId>
<version>3.4.0</version>
</dependency>
<dependency>
<groupId>org.testng</groupId>
<artifactId>testng</artifactId>
<version>6.11</version>
</dependency>
```
7. Sukurkite naują testo klasę.
Norėdami sukurti naują testą, sukurkite naują "Java" failą (klasę) ir išspręskite atvaizdus tarp rodomo tinklalapio ir parašytų parinkčių. Pasirinkėjai dažniausiai yra parašyti atskirame faile (klasėje), taigi kodas yra organizuotas. Tam naudojamos klasės yra vadinamos puslapio objektų klasės.
Kurdami testą, pereikite tarp puslapio objekto ir bandymo, kad pateiktumėte žiniatinklio elementų objektus, su kuriais dirbate.
Kiekvienas testas ar bandymų rinkinys, kurie yra susiję, turi turėti savo klasę.
Bandymas gali būti sugrupuotas su vartotojo istorijos pavadinimu.

8. Nustatykite žiniatinklio elementus ir kurkite Java objektus.
Norėdami paleisti žiniatinklio GUI automatizuotus testus, turite identifikuoti žiniatinklio elementus (pvz., Mygtukus ir įvesties laukus) puslapyje ir kurti algoritmo kodą naudodami tuos žiniatinklio elementus. Kodas gali apimti veiksmus, tokius kaip lentelėje numatytos vertės nustatymas, spustelėjimas kitame puslapyje, kai vertės rodomos keliuose puslapiuose, laukiant elemento, kuris bus rodomas išplečiamajame sąraše, arba laukiant, kol pasirodys pakrovimo dialogas.
Jūs galite perkelti žiniatinklio elementą iš naršyklės naudodami vieną iš šių metodų (funkcijų):
Java elementą galite rasti žiniatinklio elementu, naudodami metodus iš "By" klasės, pavyzdžiui:

className
cssSelector
id (String id)
pavadinimas
partialLinkText
tagName 
xpath 
ClassName 
ByCssSelector
ById
ByLinkText
ByName
ByPartialLinkText
ByTagName
ByXPath

Taigi, galite pasirinkti kaip eilutę arba perduoti pagal pavyzdį, atsižvelgiant į tai, kad pasirinkimas jau buvo sukurtas.
Tada jūs suteikiate šią funkciją selektoriaus tipą (xpath, css ar trumpesnės formos, pvz., ID, nuorodų tekstas [galima naudoti tik xpath ar css)) ir pasirinktu tekstu "// div [@ class = 'table_row'] ", Ir java konvertuos jį į java objektą.
"Chrome" naršyklė gali paryškinti identifikuotą objektą (žiniatinklio elementą), įvesdami parinktį paieškos srityje arba naudodamiesi JQuery funkcijomis. Tai galima padaryti nereikia įdiegti jokio įskiepio. Norėdami pamatyti HTML kodą, turite dešiniuoju pelės mygtuku spustelėkite puslapį ir spustelėkite "patikrinti". Norėdami sukurti selektorių, turėtumėte gerai suprasti HTML.

Pavyzdys būtų įvesti XPath selector `//div [@ class = 'table_row']` paieškos laukelyje apačioje arba $ x `("// div [@ class = 'table_row']")` konsolės srityje arba CSS parinkiklis `"div [class = 'table_row']` paieškos laukelyje ir $ $ `(" div [class = 'table_row'])` konsolėje.
"CSS" parinkiklio rašymas "Chrome" paieškos srityje:
"Web Elements" nustatymas "Firefox".
Žiniatinklio elementai pabrėžiami "Firefox" kūrėjo priemonė nenaudojant "Firebug". Tai daroma dešiniuoju pelės klavišu spustelėdami puslapį ir spustelėkite "patikrinti". Tinklalapis, kurį spustelėjote dešiniuoju pelės klavišu ir patikrinote, bus paryškintas žemiau.
9. Atlikite veiksmus elementų tinkle. 
10. Testavimas
11. Sukurti teiginius
12. Atlikite savo testą.
TestNG paleisti konfigūracijas
TestNG biblioteka pateikia šias funkcijas, kai jos importuojamos ir naudojamos.
Paketas => Nurodyti paketą paleisti. Bus pateikti visi šio paketo ir žemiau pateikti testai
Grupė => Nurodykite TestNG grupę, kurią norite paleisti
Suite => Nurodykite išorinį testng.xml failą, kurį norite paleisti
Klasė => Vykdyti visus testus vienoje klasėje
Metodas => paleiskite vieną bandymo metodą
Pattern => Visi bandymai atitinka modelį
Bandymai atliekami iš komandinės eilutės.
13. Sukurkite bandymo ataskaitą.
14. Integravimas su Git.

## Top 15 UI Test Automation Best Practices You Should Follow
https://www.blazemeter.com/blog/top-15-ui-test-automation-best-practices-you-should-follow
1. Negalima pasikliauti TIK tik UI testų automatizavimu.
2. Apsvarstykite galimybę naudoti BDD sistemą.
3. Visada visada visada naudokite bandymo dizaino modelius ir principus.
4. Niekada nenaudokite thread.sleep (), nebent yra konkrečių bandymų reikalavimų.
5. Negalima paleisti VISŲ bandymų visose tikslinėse naršyklėse.
6. Atskirkite testus iš bandymo automatizavimo sistemos.
7. Padarykite savo bandymo automatizavimo sistemą nešiojamą.
8. Pavadinkite savo testus protingai.
9. Naudokite minkštus teiginius, jei jums reikia sudaryti su tuo pačiu tinklalapiu susijusių patikrinimų sąrašą.
10. Paimkite ekrano kopijas nesėkmės tyrimui.
11. Padarykite testus paprasčiau vietoj komentarų pridėjimo.
12. Laikykitės "žaliųjų bandymų vykdymo" politikos.
13. Naudokite duomenis, o ne kartotinius bandymus.
14. Visi bandymai turi būti nepriklausomi.
15. Nustatyti išsamias automatinių bandymų ataskaitas.
(Straipsnyje punktai paaiškinti išsamiai.)

## UI Testing
https://www.guru99.com/gui-testing.html
GUI - graphical user interface. (Grafinė naudotojo sąsaja) Tai grafikos priemonėmis pagrįsta sąsaja tarp žmogaus ir kompiuterio. 
Ji yra naudojama komandoms parinkti, programoms paleisti, failų ir katalogų vardams parinktims, paramentrams stebėti bei parinkti, taip pat kitiems veiksmams atlikti naudojami ekrane rodomi dialogo langai, meniu punktai ir mygtukai, kuriais manipuliuojama pele arba klaviatūra. Naujas, perspektyvus įvedimo įrenginys yra lietimui jautrus ekranas. Su juo tuos pačius veiksmus galima atlikti liečiant ekraną ranka ar specialiu rašikliu. 

Pagrindiniai grafinės sąsajos komponentai:
 - Darbalaukis
- Langas
- Piktograma
- Meniu
- Pelės žymeklis

GUI privalumai:
- Visi taikomųjų programų langai tampa standartizuoti. 
- Visos taikomosios programos dirba pagal panašius principus, kuriuos nustato kompiuterio operacinė sistema. 
- Naudojant GUI palengvėja ir supaprastėja naujų programinių produktų kūrimas. 
Daugumoje grafinių sąsajų naudojamas įvykių valdomas programavimas. Programuotojas turi tinkamai pateikti ir užregistruoti kodą, kuris sistemos automatiškai iškviečiamas atsakant į veiksmus pele arba klaviatūra.

GUI - is a form of user interface that allows users to interact with electonic devices through graphical icons and visual indicators such as secondary notation, instead of text - based user interfaces, typed command - line labels or text navigation.

GUI - thee are two types of interfaces for a computer application.
- Command Line Interface is where you type text and computer responds to that command.
- GUI stands for Graphical user interface where you interact with the computer using images ratherthan text.
- GUI testing is a process of testing the system GUI of the aplication under test. GUI testing involves checing the screens with the controls like menus, buttons, icons, and all type of bars - toolbar, menu bar, dialog boxes snd windows, etc.
- GUI is what user sees. A user does not see the source code. The interface is visible to the user. Especially the focus is on the design stucture, omages that the are working properly or not.
- If we have to do GUI testing we first check that the images shold be comletely visible in different browsers. 
- Also, the links are available, and the button showl work when cliced.
- Also, if the user resizes the screen, neither images nor content should shrink or crop or overlap. 
