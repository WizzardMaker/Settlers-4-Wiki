---
description: by Phottor
---

# Kampfkraftberechnung

## Allgemeines

<iframe style="width: 100%;aspect-ratio:16/9;" src="https://www.youtube.com/embed/YcVu_iQ8FAo" frameborder="0" allowfullscreen></iframe>
<figcaption markdown>
Video von [UltimateSpinDash](https://www.youtube.com/channel/UCXRXmtOKDS3iX2QJDCffwLA)

</figcaption>
            

Auch wenn das Spiel die Kampfkraft intern in pro 256 verrechnet, werde ich meine folgenden Aussagen über pro Zent (%) machen, da die Kampkraft im Spiel ja auch so angegeben wird. Mit minimalen Rundungsfehlern ist zu rechnen.&#x20;

## Faktoren der Offensiven KK

Offensiv Kampfkraft wird von folgenden Faktoren beeinflusst:&#x20;

* Spielerzahl (bestimmt Startwert der KK)
* Anzahl an verbauten Ressourcen (erhöht während des Spiels die KK: mehr Bauen -> höhere Kampfkraft)
* Anzahl an vollständigen Zierobjekt-Sets, also alle 12 Objekte 1 mal gebaut (zählt auf die verbauten Ressourcen oben drauf).&#x20;

## **Berechnungsformel**

`ATK = (256*(STEIN + HOLZ + 2*GOLD + 3*ZIERSTEIN + 3*ZIERHOLZ + 6*ZIERGOLD )+127)//1000 + START + ZIERSETS*30`

`KK = ATK*100//256`

STEIN, HOLZ, GOLD = verbaute Ressourcen\
ZIERSTEIN, ZIERHOLZ, ZIERGOLD = in Zierobjekten verbaute Ressourcen\
START = Startwert abhängig von Spielerzahl\
ZIERSETS = Anzahl vollständige Zierobjektsets

### **Ressourcenwerte**

* 1 verbautes Holz oder 1 verbauter Stein sind 1 Ressource wert
* 1 verbautes Gold (nur in Tempeln möglich) ist 2 Ressourcen wert
* 1 in Zierobjekten verabautes Holz oder 1 in Zierobjekten verbauter Stein sind 3 Ressourcen wert
* 1 in Zierobjekten verbautes Gold ist sogar 6 Ressourcen wert
* 1 vollständiges Set Zierbobjekte gibt einen zusätzlichen Bonus von ungefähr 117 Ressourcen

### **Zierobjekt Ressourcen**

Ein vollständiges Zierobjekte Set (jedes der 12 Zierobjekte genau ein mal) benötigt bei den 4 Völkern Holz/Stein/Gold:

* \[R] : 18H 40S 26G = 330 Ressourcen
* \[W] : 24H 23S 27G = 303 Ressourcen
* \[M] : 9H 56S 30G = 375 Ressourcen
* \[T] : 17H 46S 31G = 375 Ressourcen

obendrauf erhält man noch die 117 Ressourcen als Setbonus.

### KK Schwellenwerte für Ressourcen

In der Formel ist zu beachten, dass diese Zahlen ab ein paar Schwellenpunkten nur noch langsamer ansteigen können. Ähnlich wie beim Gehalt, ab einem bestimmten Bruttoeinkommen, müsst ihr von jedem weiteren € etwas mehr abgeben als von den vorangehenden €.&#x20;

Hier liegen diese Schwellen bei KK 50, 100 und 125 oder bei entsprechenden ATK Werten 128, 256 und 320. Bei jeder dieser Schwellen wird der Teil, der für euch als KK nutzbar wird halbiert. Das bedeutet für eine KK im Bereich von \[min, max] kommt könnt ihr sie so "schnell" erhöhen:

* \[25, 50] : jede Ressource fließt zu vollen Teilen in die KK ein
* \[51, 100] : jede weitere Ressource fließt zu 50% in die KK ein (äquivalent zu 50% Steuern)
* \[101, 125] : jede weitere Ressource fließt zu 25% in die KK ein (75% Steuern)
* \[126, 150] : jede weitere Ressource fließt zu 12.5% in die KK ein (87.5% Steuern)

im Programm werden der Reihe nach diese Rechnungen durchgegangen:

* wenn ATK > 128, dann ATK = 128 + (ATK-128)//2
* wenn ATK > 256, dann ATK = 256 + (ATK-256)//2
* wenn ATK > 320, dann ATK = 320 + (ATK-320)//2

### Vereinfachte Faustregel

**E**ine Ressource wird in dieser Formel mit 256 multipliziert, durch 1000 dividiert, und bei der Umrechnung in % wieder mit 100 multipliziert und durch 256 dividiert.&#x20;

\
**Fazit:** 1 Ressource entspricht 0.1 KK Prozentpunkten! Das bedeutet unter Berücksichtigung der Schwellenpunkte benötigt man im KK-Bereich \[min, max] so viele Ressourcen, um die KK um einen Prozentpunkt zu erhöhen:

* \[25, 50] : 10 Ressourcen pro %-Punkt
* \[51, 100] : 20 Ressourcen pro %-Punkt
* \[101, 125] : 40 Ressourcen pro %-Punkt
* \[126, 150] : 80 Ressourcen pro %-Punkt



**KK Schub durch komplettes Zierobjekt Set (danke @Ablmeo!)**\
Nicht berücksichtigt sind dabei die Schwellenübergänge. Da zählt nur der Wert bis zur Schwelle und alles darüber nur die Hälfte.

<figure><img src="../../assets/kk.png" alt=""><figcaption></figcaption></figure>

## Starkampfkraft

Bei dieser Spielerzahl erhält man folgende Startkampfkraft:&#x20;

* 8 : \[25%] (START=64)
* 7 : \[27%] (START=69)
* 6 : \[30%] (START=76)
* 5 : \[33%] (START=85)
* 4 : \[37%] (START=96)
* 3 : \[42%] (START=109)
* 2 : \[50%] (START=128)
* 1 : \[55%] (START=153)&#x20;

bei der Prozentzahl wurde die 50% Schwelle bereits berücksichtigt, siehe 4.

## Formel Defensiv KK

wie sich die Defensiv KK aus der Offensiv KK errechnet wissen bestimmt alle:

`DKK = max(100, 100+(OKK-100)//2)`
