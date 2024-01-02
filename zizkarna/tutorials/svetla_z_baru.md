
#tutorial #Žižkárna 

# Světla v Danceroomu z baru

## Budeme potřebovat

Doslova skoro nic, ale něco jo.

- bílá světelná krabička s kabelem (ve Vojtěch šuplíku)
- Vojtěchovo počítač (PIN je __7432563__)
- Launchpad (jde to i bez něj, ale bude to lepší s ním, lol)

## Zapojení

Když se bude držet pořadí, bude to jednodušší.

1. na rozvaděči shodit první jistič (pokud je nahozený)
2. do zásuvky na rozvaděči s označením 1 zastrčit bílého psa
	nad rozvaděčem - __primární pes__
3. do splitteru přepojit správné XLR
	- splitter je ta černá krabička, co visí v rohu Danceroomu u rozvaděče za tou hnusnou trubkou a má jeden vstup _DMX IN_
	- někde v tom rohu visí dvě XLRka nadepsaný _DMX FOH_ (to je do režie, modrej kabel) a _DMX BAR_ (to je to, co je provlečený zdí na bar, černej kabel)
	- do splitteru zastrčit _DMX BAR_, protože chceme ovládat světla z baru
4. na rozvaděči nahodit první jistič
5. do počítače (na lednici, tam jako ho mám vždycky, vždyť víte, hned okamžitě ho strčte na nabíječku, kde zůstane po celou dobu používání) přes USBčka zapojit Launchpad a světelnou krabičku
6. do světelný krabičky připojit XLR, co je vyvedené na lednici skrz zeď
7. zapnout hazer a zkontrolovat stav kapaliny (kdyby málo kapaliny, bude v dílně kanistr)

## Píšu předem, kdyby bylo potřeba, vraťte se k této kapitole
- občas se stává, že velkým hlavám nejdou zapnout/vypnout výbojky skrz DasLight ani po x minutách čekání
- já vždycky čekám třeba "cigáro, pití, hajzl" minut, pak to vzdávám a posutupuju následovně
	1. k hlavě, co nechce spolupracovat vylezu po štafličkách
	2. nad displejem jsou 4 tlačítka _up_, _down_, _enter_ a _mode_
		- prosím, vyvarujte se mačkání tlačítka _mode_, těžko se z toho dostává ven :D
	3. tlačítkama _up_ a _down_ se proklikám na záložku __LAMP__
	4. stisknu _enter_
	5. podle situace pomocí tlačítek _up_ a _down_ zvolím, jestli chci výbojku zapnout __ON__ nebo vypnout __OFF__
	6. potvrdím _enter_ 
	7. a lezu dolů checheche

## Jak svítit

1. na počítači otevřít program __DasLight5__ (bude na ploše se vším potřebným)
2. DasLight se po otevření zeptá, jestli chceme používat připojenou bílou světelnou krabičku
	- zeptá se formou bílého vyskakovacího okna, kde stačí jenom stisknout __Start__
3. otevřeme uloženou scénu, je na ploše a jmenuje se __drfinal.dvc__
4. DasLight se OPĚT zeptá, jestli chceme použít bílou světelnou krabičku
	- stejný postup, jako v kroku 2.
5. důležité nažhavit výbojky (žárovky) ve velkých hlavách:
	- DasLight je rozdělen na dvě půly, horní  půlka představuje __Scény__ a spodní půlka __Nastavení__, ta je rozdělená na __Mapu__ a __Parametry__
	- na dělící čáře jsou __Skupiny__
	1. ze Skupin vybrat skupiny _hlavy velky_
	2. zkontrolovat, že se na Mapě vybraly obě velký hlavy (symetricky dva čtverečky po stranách)
	3. v menu Parametrů přejít do záložky _Other_
	4. na sloupci _Function_ kliknout na jedinou rozsvícenou žárovku (zakroužkovaná červeně)
	5. v horní části okna Parametrů kliknout na ikonku rozsvíceného světla (zakroužkovaná červeně)
	6. počkat, než se obě hlavy rozsvítí
	   ![[daslight_layout.jpg]]
6. pokud obě hlavy svítí, tak v okně Parametry vyresetovat všechny parametry:
	1. v každé záložce (_Other_, _Beam_, _Color_, _Dimmer_) kliknout na všechny žluté puntíky
	2. pokud je záložka resetovaná, přestane u jejího názvu svítit žlutá tečka
	   ![[daslight_reset.png]]
7. v Parametrech se přepnout z módu _Live_ do módu _Edit_
8. zkontrolujeme, zda je připojený Launchpad 
	- (tři tečky tlačítko, pravej horní roh) > "Edit" > "Settings..." > "MIDI / Audio / BPM" > MIDI Devices
	- u zařízení _MIDIIN2 (LPX MIDI)_ a _MIDIOUT2 (LPX MIDI)_ zakliknout všechny škrtátka
	  ![[daslight_midi.jpg]]
9. na Launchpadu přepnout na správnou banku: > Custom > __Send B__
10. sloupce na Launchapdu korespondují se sloupcema v DasLightu, konkrétně:
	1. velký hlavy - pozice/pohyby
	2. velký hlavy - gobo (gobo je ta "šablona," skrz kterou svítí to světlo a dělá různý efekty - např. místo jednoho kola svítí hvězda apod.)
	3. velký hlavy - prism/hranol (dvě polohy - prism ON a prism OFF, pokud je ON, tak bude světlo roztříštěno do tří identických světel)
		- nestihl jsem naprogramovat, takže sloupec můžete klidně  vyignorovat, sorry :/
	1. malý hlavy - pozice/pohyby
	2. barvy a barevný efekty
	3. blindery - mačkací, po stisknutí/podržení svítí statická bílá, postupně odshora: LED vany, velké hlavy a malé hlavy
	4. hazer - bílý sloupec dole, odspodu 10 %, 50 % a 100 % (100 % nutno držet)
	5. žlutý sloupce ignorovat
	- pohyby, prism, goba a barevný efekty lze kombinovat, blindery přebíjí všechno (pokud běží barevnej efekt a stiskne se blinder, blinder má přednost)
	- růžová tlačítka u pozic/pohybů je statická pozice - natočení do lidí, připraveno na blinder
	- doporučuju si k tomu sednout a zapnout světla podle druhýho PDFka "svetla_danceroom_foh.pdf" a zjistit si, co co dělá, dkyž u toho sedíte, ať to pak z baru klikáte nějak automaticky bez toho, aniž byste se tam museli chodit koukat ;)

## Vypínání, aneb zhasněte lampiony já chci vidět tmu

Postup neni těžkej, naopak

1. vypnout hazer vypínačem zezadu
2. přes launchpad vypnout všechny efekty a pohyby, prostě odkliknout, co je zakliknutý
3. v Parametrech se přepnout z módu _Edit_ do módu _Live_
4. vypnout a zchladit velký hlavy, výbojky (obdobný pustup, jako při jejich zapínání):
	1. ze Skupin vybrat skupiny _hlavy velky_
	2. zkontrolovat, že se na Mapě vybraly obě velký hlavy (symetricky dva čtverečky po stranách)
	3. v menu Parametrů přejít do záložky _Other_
	4. na sloupci _Function_ kliknout na jedinou zhasnutou žárovku (zakroužkovaná červeně)
	5. v horní části okna Parametrů kliknout na ikonku zhasnutého světla (zakroužkovaná červeně)
	![[daslight_off.jpg]]
5. počkat, než se obě hlavy zhasnou
	- může se zdát, že jsou hlavy vypnutý, protože nesvítí světlo na zem
	- ale ta výbojka svítí pořád, dokud se nezchladí, jenom je zakrytá
	- jestli výbojka svítí je vidět skrz větrací průduchy na těle hlavy (potřeba mít v místnosti absolutní tmu)
	- Hlava s nezchlazenou výbojkou: ![[hlava_waiting0.jpg]]
	- Hlava co svítí (pro porovnání jak svítí hlava, co má svítit a jak svítí hlava s nezchlazenou výbojkou): ![[hlava_on.jpg]]
6. pokud jsou obě hlavy zhasnuté, shodit první jistič
7. uklidit, co je potřeba uklidit a hotovo