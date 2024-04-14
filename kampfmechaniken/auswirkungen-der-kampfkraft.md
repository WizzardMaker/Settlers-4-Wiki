---
description: by Phottor
---

# Auswirkungen der Kampfkraft

## Erklärung

Wenn eine Einheit angreift, dann wird ihr Schadenswert mit der Kampfkraft multipliziert, danach eventuell durch Zauber wie Blutrausch oder Schildzauber verdoppelt oder halbiert und als letztes wird der Rüstungswert abgezogen (nur gegen Hauptmänner relevant).&#x20;

Der so errechnete Schaden wird der gegnerischen Einheit von ihren Hitpoints abgezogen. Fallen diese HP auf oder unter 0, stirbt die Einheit. Wenn sich die angreifende Einheit auf eigenen/verbündeten Land befindet, wird die defenisve Kampfkraft zur Berechnung des Schadens genutzt, auf neutralen/gegnerischen Land die offensive Kampfkraft.&#x20;

Bei der Multiplikation des Schadenswertes mit der Kampfkraft erhält man eine Kommazahl, diese wird auf eine natürliche Zahl gerundet (ab x,48 wird ungewöhnlicherweise aufgerundet auf x+1, worauf das zurückzuführen ist, ist mir nicht 100% klar).

**Eine Einheit kann nur eine natürliche Zahl an Hitpoints haben/verlieren. Dieses Aufrunden führt dazu, dass eine bestimmte Einheit, ab einem konkreten KK-Schwellenwert 1 Schaden mehr austeilt als mit nur 1KK weniger.**

Zum Beispiel teilt ein Schwertkämpfer auf 100KK 20 Schaden aus, auf 102KK teilt er 20.4=20 Schaden aus und auf 103KK teilt er 20.6=21 Schaden aus.&#x20;

Das ist also eine recht abrupte Grenze, wo bestimmte Einheiten stärker werden. Wenn die Schadenserhöhung ausreicht, sodass man einen Schlag weniger braucht, um eine gegnerische Einheit zu töten, so sprechen wir von einem **KK-Tick/Spike**.&#x20;

Man beachte, dass z.B. ein 21 Schaden Schwertkämpfer und ein 22 Schaden Schwertkämpfer jeweils 10 Schläge brauchen, um einen gegnerischen Schwertkämpfer mit 210HP zu töten. In einer reinen Schwertkämpfer Armee sind sie also effektiv gleich stark.

## **Die KK Ticks von L3 Einheiten**

für die wichtigsten Armeenkonstellationen aus reinen L3 Einheiten habe ich die KK-Ticks und die Anzahl Hits per Kill übersichtlich zusammengefasst:&#x20;

_1. Zeile KK Spikes_ \
_2. Zeile Hits per Kill_&#x20;


=== "Schwert KK gegen Schwert"
	**Schwert KK gegen Schwert**
	
	`25 - 28 - 33 - 38 - 43 - 48 - 53 - 58 - 63 - 68 - 73 - 83 - 88 - 98 - 103 - 118 - 133 - 148`
	
	`42 - 35 - 30 - 27 - 24 - 21 - 20 - 18 - 17 - 15 - 14 - 13 - 12 - 11 - 10  - 9   - 8   - 7`


=== "Schwert KK gegen Bogis"
	**Schwert KK gegen Bogis**
	
	`25 - 28 - 33 - 38 - 43 - 48 - 53 - 58 - 63 - 68 - 73 - 78 - 88 - 98 - 113 - 133`
	
	`32 - 27 - 23 - 20 - 18 - 16 - 15 - 14 - 13 - 12 - 11 - 10 - 9  - 8  - 7   - 6`


=== "Bogi KK gegen Bogis"
	**Bogi KK gegen Bogis** (gleiche Spikes gegen alle anderen Einheiten)
	
	`25 - 32 - 44 - 57 - 69 - 81 - 94 - 106 - 119 - 131 - 144`
	
	`80 - 54 - 40 - 32 - 27 - 23 - 20 - 18  - 16  - 15  - 14`



****

An den Hits per Kill lässt sich erkennen, dass z.B. bei Bogenschützen vs. Bogenschützen der Sprung von 106KK \[18 Hits per Kill] auf 119KK \[16 Hits per Kill] einer Truppenverstärkung von 11% gleichkommt, während der Sprung von 119KK \[16 Hits per Kill] auf 131KK \[15 Hits per Kill] nur ungefähr einer Verstärkung von 6% gleicht. Das gilt es auch zu berücksichtigen, wenn man von "Spieler X hat 1 KK Tick mehr als Spieler Y" spricht.

## KK Tabelle aller Einheiten

Nightfever221 hat eine größere Tabelle angefertigt für die Standardeinheiten beliebigen Levels (danke!): Beachtet allerdings, dass manche Einträge aufgrund des merkwürdigen Rundens in Siedler 4 in dieser Tabelle um einen Wert zu hoch sind (z.B. braucht man nur 131KK, um einen L3 Bogenschützen mit 15 Hits zu töten, nicht 132). Wenn ihr euch an diese Tabelle haltet, so nehmt ihr aber definitiv alle KK-Spikes mit.

<figure><img src="../../assets/table.png" alt=""><figcaption></figcaption></figure>

## KK für Spezialeinheiten (not yet available)

Für alle anderen Einheiten (Spezialeinheiten) gibt es aktuell noch keine Tabelle. Ihr könnt euch aber relativ einfach ausrechnen, ab wann eure Spezialeinheiten mehr Schaden machen:&#x20;

Ein Rucksackkatapultist L3 macht z.B. 13 Schaden, d.h. alle 1/13 = 0.0769.. = 7.69KK erhöht sich sein Schaden um 1. Aufgerundet wird ab der Hälfte, also ist der erste Spike nach 100 bei 103.84=104KK.&#x20;

Danach geht es in 7.69KK Schritten weiter. Rucksackkatapultisten haben noch die Besonderheit mit ihrem Flächenschaden. Durch das "Durcheinander" an Damage Dealern, kann man auch die Hits per Kill nicht mehr so eindeutig ausrechnen. Das hat man aber prinzipiell wenn man verschiedene Armeen mehrerer Spieler (z.T. auch mit unterschiedlicher KK) durcheinander mischt.&#x20;

**Selbstverständlich gilt aber**: je mehr Schaden, desto besser. Vermutlich gibt es auch verschieden "gute" Spikes für Rucksackkatapultisten, je nachdem, ob ein Spike auch den Flächenschaden eines oder beider seiner Radien um 1 erhöht.
