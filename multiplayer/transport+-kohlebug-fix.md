# Transport+ / "Kohlebug"fix

<iframe style="width: 100%;aspect-ratio:16/9;" src="https://www.youtube.com/embed/NSWV3QzbWQU" frameborder="0" allowfullscreen></iframe>
<figcaption markdown>
Video von [UltimateSpinDash](https://www.youtube.com/channel/UCXRXmtOKDS3iX2QJDCffwLA)

</figcaption>
            

## Was ist der Kohlebug?

Siedler4 ist zu einer Zeit entstanden, wo herkömmliche Prozessoren noch 500 Mhz hatten. Um diese nicht zu überfordern wurde von den Spieleentwicklern damals ein Limit eingebaut, wieviele Waren eines Typs angefordert werden. \
Das Spiel arbeitet intern mit sogenannten "Ticks" - pro Sekunde werden ca. 14 Ticks ausgeführt. Das Limit, welches von den Entwicklern hier eingebaut wurde, sieht nun vor das lediglich eine Einheit pro Warentyp alle 16 Ticks in die Transportwarteschlange (Queue) gegeben werden kann. Dies entspricht Rechnerisch ca. 52 Einheiten, die pro Spielminute so angefordert werden können.

Nur wenige spezielle Waren werden direkt zweimal angefordert - Baustoffe und Kohle. Somit können maximal 104 Kohleeinheiten pro Minute von den Gebäuden angefordert werden. Dies ist auch anders bekannt als der sogenannte [HE Ausbau](../produktionsverhaeltnisse/he-ausbau-2-zu-1-gold.md), bei dem gezielt dieses Limit ausgenutzt wird um die größtmögliche Menge an L3 Soldaten zu produzieren.&#x20;

## Der eigentliche Fix

Der Entwickler nyfrk hat vor einigen Jahren einen Workaround geschrieben, um diese künstliche Limitierung massiv auszuweiten. Diese ist veröffentlicht auf [Github ](https://github.com/nyfrk/Settlers4-Coalfix)und entsprechend als Transport+ in [Settlers United](settlers-united.md) integriert.&#x20;

Dieser Fix setzt nun die Zeit von 16 Ticks auf 1 Tick runter. Wodurch das Limit für sämtliche Waren somit um den Faktor 16x angehoben wird. Theoretisch sind nun 1664 Kohleaufträge pro Minute möglich.&#x20;

## Nebeneffekte

Dieser Fix hat verschiedene Auswirkungen. Zum einen reagieren eure Siedler nun deutlich schneller auf entsprechende Trageaufträge - anstatt vorher über 1 Sekunde zu warten, laufen sie nun unmittelbarer los. **Dies bedeutet insbesondere für eure Kasernen, das diese nun deutlich effektiver werden und schneller Soldaten ausbilden können!** (Vorallem wenn Waffen & Gold sich  in einem benachbartem Lager befinden)

Jedoch benötigt ihr hierdurch auch deutlich mehr Siedler im Endgame. Es wird alles immer direkt unmittelbar getragen, wodurch eure Siedler deutlich mehr beschäftigt sind.&#x20;
