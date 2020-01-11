# rubrik-erkennung
Das Python-Skript erkennt die Rubrik von (journalistischen) Texte.

Folgende Rubriken werden erkannt:
* Politik
* Panorama
* Sport
* Wirtschaft
* Kultur
* Technik
* Reise
* Auto
* Gesundheit
* Wissen

Das Skript beruht auf einem Texkorpus hunderttausender Spiegel-Online-Artikel und erstellt die Zugehörigkeitswahrscheinlichkeit eines Eingabetextes zu einzelnen Rubriken. Im Zweifel wird None zurückgegeben.

## So funktioniert's
```
from get_rubrik import get_rubrik

text= "Randers (Dänemark), 30.11.2019 – Bei der 72. Dreiband-Weltmeisterschaft im dänischen Randers holte sich der 57-jährige Schwede Torbjörn Blomdahl seine sechste Goldmedaille nach 1987, 1988, 1991, 1997 und 2015. Im Finale schlug er den Vietnamesen Nguyễn Đức Anh Chiến mit 40:37 in 22 Aufnahmen. Nguyễn ist damit der erste vietnamesische Vize-Weltmeister in dieser Disziplin. Vor ihm konnten seine Landsleute Mã Minh Cẩm (2017) und Nguyễn Quốc Nguyện (2018) eine Bronzemedaille gewinnen. Einzige asiatische Sieger waren bisher die Japaner Nobuaki Kobayashi (1974, 1984), dessen Todesnachricht bei der Eröffnungsrede von Herbert Thür, Sportdirektor des Weltverbandes Union Mondiale de Billard (UMB), bekannt gegeben wurde und für Betroffenheit, vor allem unter den älteren Spielern, die noch mit ihm spielten, sorgte, Ryūji Umeda (2007) und der Koreaner Choi Sung-won (2014)." # Quelle des Beispieltexts: https://de.wikinews.org/wiki/Der_Schwede_Blomdahl_holt_sich_sein_sechstes_WM-Gold


rubrik = get_rubrik(text)
print(rubrik)
```
Ergebnis:
```
Sport
```
