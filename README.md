# Gudhotn - dialekt Budhót'nu

Dialekt umělého jazyka na bázi slovanských jazyků s redukovaným repertoárem grafémů a fonémů. 0. verze.

Jména souborů mají v sobě stále "budhotn" pro zpětnou kompatibilitu a možnost zpětného mergeování.

+ **budhotn.csv** - strojově čitelný slovník, přímo zde vyhledávatelný (5000+ řádků)
    - Kombinuje: slovíčka, fráze, koncovky, předpony, číslovky (část), větné členy
+ **budhotn_abeceda.csv** - abeceda a výslovnost (výhledově i šifry)
+ **budhotn_postatna.csv** - tabulka skloňování podstatných jmen
+ **budhotn_pridavna.csv** - tabulka skloňování přídavných jmen
+ **budhotn_zajmena.csv** - tabulka skloňování zájmen
+ **budhotn_cislovky.csv** - číslovky a tabulka jejich skloňování
+ **budhotn_slovesa.csv** - tabulka časování sloves
+ **README.md** - tento informační soubor

Původní Excelovský sešit **Budhót'n.xslx** viz původní repozitář. Obsahuje listy: abeceda, slovíčka, fráze, pod.jm., koncovky, příd.jm., slovesa, předpony, zájmena, číslovky, členy, zkratky, velká písmena


## Kontakty

Budhót'n vytváří [classroomtoilet](https://classroomtoilet.cz/), repozitář udržuje a Gudhotn vytváří [637man](https://getmania.blogspot.com/).

[Skupina na Facebooku (aktualizace Budhót'n.xlsx)](https://www.facebook.com/groups/261329611863060)


## Kterak psáti znaky nabodlé

Budhót'n byl vymyšlen pro českou klávesnici a Gudhotn se toho drží. Ta má ve Window$ na AltGr (pravý Alt) a číselné řadě různé mrtvé klávesy, o nichž řada uživatelů pravděpodobně neví. V Linuxu je nutné použít Shift+AltGr, neboť AltGr na číselné řadě přeřazuje na symboly z americké klávesnice. Macintosh ani Amigu nikdo z autorů nemá, takže nemůže ověřit.

  AltGr: | ~ | ~ | ˇ | ^ | ˘ | ° | ˛ | \` | ˙ | ' | ˝ | " | ¸
:--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---:
Příklad: | ~ | ã | ǎ | â | ă | å | ą | à | ȧ | á | ő | ä | ç
  Shift: | ° | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 0 | % | ˇ
  Běžně: | ; | + | ě | š | č | ř | ž | ý | á | í | é | = | ´

Na Window$ jsou omezenější možnosti nabodávání než na Linuxu. Rovněž nefunguje prstolamné Ctrl+Shift+U. [DOSový zlozvyk levého Altu](https://en.wikipedia.org/wiki/Alt_code) umožňuje pouze DOS Latin a s úvodní 0 Window$ Latin (>255 funguje v závislosti na aplikaci), pokud není "HKEY_CURRENT_USER\Control Panel\Input Method\EnableHexNumpad" == "1", to pak umožňuje použití úvodního + a je hexadecimální. Gudhotn je vytvářen na Linuxu, kde jsou [častěji aktualizované](https://cgit.freedesktop.org/xorg/lib/libX11/log/nls/en_US.UTF-8/Compose.pre) [skladné sekvence X11](https://cgit.freedesktop.org/xorg/lib/libX11/plain/nls/en_US.UTF-8/Compose.pre).

          Základ                        Shift                     Linux AltGr              Linux Shift+AltGr
    q w e r t z u i o p ú )     Q W E R T Z U I O P / (     \ | € ¶ ŧ ← ↓ → ø þ [ ]     Ω Ł E ® Ŧ ¥ ↑ ı Ø Þ ÷ ×
    a s d f g h j k l ů § "     A S D F G H J K L " ! '     ~ đ Đ [ ] ` ' ł Ł $ ' \     Æ § Ð ª Ŋ Ħ ̛  & Ł ˝ ß |
     y x c v b n m , . -         Y X C V B N M ? : _         ° # & @ { } ^ < > *         < > © ‘ ’ N º × ÷ ˙

Mrtvá tečka nahoře se chová zvláštně v případě I: ı a İ, té se však v Gudhotnu nepoužívá. Dále jsou na české klávesnici méně obskurní mrtvá tlačítka na kroužek (Shift+;), čárku (vedle Backspace), háček (Shift+´) a přehlásku. Přehláska je na té klávese, která je pokaždé někde jinde poblíž Entru/Return/<-', a pod Shiftem se na ní ukrývá apostrof. Na linuxové americké mezinárodní klávesnici s AltGr mrtvými tlačítky nelze napsat đ, jen ð, ale to se považuje za variantu. Podobně je místo Ŧ/ŧ možné psát Þ/þ. Momentálně nejde libovolně kombinovat více nabodeníček pro emulaci abdžádu. Seznam nabodlých písmenek nominálního zápisu, tedy ani spřežky, ani zkratky:

Písmeno | Klávesy | Unicode
--- | --- | ---
Á á | 8 / AltGr+9,A | U+00C1 U+00E1
Č č | 4 / Shift+´,C / AltGr+2,C | U+010C U+010D
Ď ď | Shift+´,d / AlrGr+2,D | U+010E U+010F
Đ đ | AltGr+D (malé AltGr+S) | U+0110 U+0111
Ð ð | AltGr+D (US mezinárodní) | U+00D0 U+00F0
É é | 0 | U+00C9 U+00E9
Í í | 9 | U+00CD U+00ED
Ĺ ĺ | ´,L / AltGr+9,L | U+0139 U+013A
Ľ ľ | Shift+´,L | U+013D U+013E
Ň ň | Shift+´,N / AltGr+2,N | U+0147 U+0148
Ö ö | ¨,O / AltGr+=,O | U+00D6 U+00F6
Ó ó | ´,O | U+00D3 U+00F3
Ő ő | AltGr+0,O | U+0150 U+0151
Ŕ ŕ | ´,R / AltGr+9,R | U+0154 U+0155
Ř ř | 5 / AltGr+2,R | U+0158 U+0159
Š š | 3 / AltGr+2,S | U+0160 U+0161
Ť ť | Shift+´,T / AltGr+2,T | U+0164 U+0165
Ŧ ŧ | AltGr+T | U+0166 U+0167
Þ þ | AltGr+P | U+00DE U+00FE
Ü ü | ¨,U / AltGr+=,U | U+00DC U+00FC
Ú ú | Ú / AltGr+9,U | U+00DA U+00FA
Ű ű | AltGr+0,U | U+0170 U+0171
Ý ý | 7 / AltGr+9,Y | U+00DD U+00FD
Ž ž | 6 / AltGr+ě+Z | U+017D U+017E
