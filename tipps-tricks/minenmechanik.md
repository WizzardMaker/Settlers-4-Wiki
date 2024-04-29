---
description: by Phottor
---

# Minenmechanik

## **Minenmechaniken in Siedler 4**&#x20;

(aufbauend auf dem sehr guten Video von @SpinniD: [https://www.youtube.com/watch?v=sKXNqzNjd9w](https://www.youtube.com/watch?v=sKXNqzNjd9w)) Es wurde zwar letztens schon fleißig über das Koordinatensystem (hexagonal) diskutiert, aber hier nochmal zur Veranschaulichung ein Bild. Das Beispiel zeigt eine 4x4 große Map, üblich ist 1024x1024.

<figure><img src="https://media.discordapp.net/attachments/576807103256068102/850485568399343686/unknown.png?width=388\&height=300" alt=""><figcaption></figcaption></figure>

**1.** Geologen setzen beim Beschildern niemals zwei Schilder an benachbarte Felder (mindestens 1 Feld frei zwischen zwei Schildern, oftmals lassen sie auch 2-3 Felder Abstand). **Ausnahme:** Wenn zwei Geologen direkt nebeneinander stehen und gleichzeitig ihr Schild in den Boden Klopfen, dann und nur dann stehen die Schilder ohne Mindestabstand&#x20;



**2.** Unterirdisch hat ein Ressourcenvorkommen einen Füllgrad von 1 bis 15. Dies entspricht genau der Anzahl an vorhandenen Ressourcen (Kohle, Eisen, etc.) in diesem Feld. Wird von diesem Feld eine Ressource gefördert, so reduziert sich der Füllgrad um 1. Wenn ein Geologe ein Schild auf ein Vorkommen stellt, dann wird dieses bei Füllgrad 1 bis 5 zu einem 1er Schild, bei Füllgrad 6 bis 10 zu einem 2er Schild und bei Füllgrad 11 bis 15 zu einem 3er Schild



**3.** Der Erzgenerator von Siedler IV ist unterschiedlich im Editor und im Spiel (führe das darauf zurück, dass der Editor noch den GE Generator benutzt). Genaue Tests sind leider nur im Editor möglich, aber ich habe zumindest sichergestellt, dass keine schwerwiegenden Unterschiede vorliegen, indem ich einen Geologen 20x die gleiche Stelle hab abstecken lassen und "mitgeschrieben" habe. Auf Zufallskarten (also dann wenn ein Berg generiert wird) sind die jeweiligen Gold-, Eisen-, Kohle-, Stein- und Schwefelvorkommen IMMER von exakt gleicher Form und Größe. 



Zur Veranschaulichung jeweils exemplarisch eins von allen Vorkommen. Das bedeutet, unabhängig davon wie geschickt sich unsere Geologen anstellen (ob sie jetzt bei einem Goldvorkommen nur 1 Schild finden, oder 5), das Vorkommen an dieser Stelle ist immer gleich groß und gleich geformt! 

**Ausnahme:** Wenn ein Vorkommen am Rand zur Wiese oder Schnee oder direkt auf der Spiegelachse generiert wird, kann es abgeschnitten werden. Ebenso kann es von einem anderen Vorkommen welches links oder oberhalb direkt daneben generiert wird überschrieben werden. Auf HGxx haben alle Schilder Füllgrad 15, d.h. wirklich jedes Vorkommen ist identisch. Auf MGxx oder LGxx spielt bei dem Füllgrad ein Zufallsfaktor mit rein, aber der durchschnittliche Füllgrad eines Vorkommens sollte nicht allzu varianzbehaftet sein. Das heißt aber auch, selbst wenn der Geologe auf LGLG nur ein einziges 1er Goldschildchen absteckt, das Vorkommen unten drunter ist eigentlich ganz vernünftig, potentiell sogar gleich gut, wie wenn er vier 3er Schildchen absteckt. 



**Ausnahme2:** Es stellte sich raus, dass super selten ein Vorkommen nicht die von mir beschriebene Form (48 Schilder bei Kohle, 24 bei Eisen/Stein/Schwefel, 18 bei Gold) hat, sondern stattdessen ein 16 Schilder Vorkommen entsteht. Ich tippe ganz stark auf einen Bug, der passiert nach ein paar Test Maps bei 0-3 Vorkommen pro gesamte Map. 16 Schilder hat zur Folge, dass eine Kohlemine nur 33% von einer perfekt platzierten „normalen“ Mine hat, eine Eisenmine 66% und eine Goldmine 89%. Verbuggte Kohlevorkommen kann man relativ einfach erkennen, einfach weil diese in ihrer Fläche deutlich kleiner sind als man es gewohnt ist. Bei Eisen/Stein/Schwefel/Gold hat man denke ich keine Chance das in game zu erkennen, der Effekt ist aber auch nicht ganz so gravierend (credits an @LA-TheGGend). So wie es aussieht werden Vorkommen von rechts nach links, Reihe um Reihe von unten nach oben generiert. Beim Generieren werden die Nachbarn überschrieben, d.h. obere Vorkommen überschreiben potentiell untere, linke überschreiben potentiell rechte, aber oben rechte überschreiben trotzdem unten linke. 



**Achtung:** Meine Aussagen und Formen gelten für eine ungespiegelte Karte. Auf einer gespiegelten Karte verhält es sich im linken Quadranten genauso, in den übrigen Quadranten werden die Vorkommen gespiegelt und haben dementsprechend eine leicht andere Form. Auch wird der Teil gespiegelt, wo sich Vorkommen überschneiden: das rechte untere Vorkommen kann auf einer gespiegelten Hälfte das links obere überschreiben.

<figure><img src="https://media.discordapp.net/attachments/576807103256068102/850486077604364348/unknown.png" alt="Gold"><figcaption>Gold</figcaption></figure>

<figure><img src="https://media.discordapp.net/attachments/576807103256068102/850486127903375410/unknown.png" alt="Kohle"><figcaption>Kohle</figcaption></figure>

<figure><img src="https://media.discordapp.net/attachments/576807103256068102/850486164652818432/unknown.png" alt="Eisen"><figcaption>Eisen</figcaption></figure>

<figure><img src="https://media.discordapp.net/attachments/576807103256068102/850486195997638656/unknown.png" alt="Stein"><figcaption>Stein</figcaption></figure>

<figure><img src="https://media.discordapp.net/attachments/576807103256068102/850486232282955836/unknown.png" alt="Schwefel"><figcaption>Schwefel</figcaption></figure>

**4.** Eine Mine die auf die mit 'X' markierte Koordinate gesetzt wird hat den folgenden Arbeitsbereich. Aus diesen 64 Feldern kann der Minenarbeiter fördern. Das bedeutet mit einem maximalen Füllgrad von 15, kann eine einzige Mine maximal 64\*15=960 Ressourcen fördern. Da gegen Ende die Effizienz abnimmt, muss man allerdings ein Hundertfaches der Lieblingsnahrung bereitstellen, um wirklich die letzten 10 Ressourcen rauszukratzen. Der Minenarbeiter kann übrigens auch Felder in seinem Arbeitsbereich bearbeiten, die außerhalb der eigenen Landesgrenze liegen.&#x20;

<figure><img src="https://media.discordapp.net/attachments/576807103256068102/850486375865778246/unknown.png?width=388\&height=300" alt="Bild"><figcaption>Bild</figcaption></figure>

**5.** Für eine Lieblingsnahrung macht der Minenarbeiter 10 Minengänge, für falsche Nahrung 2 Minengänge und unmittelbar nach dem Bau der Mine macht er ohne Nahrung kostenlos 10 Minengänge. Bei einem Minengang wählt der Minenarbeiter zufällig (gleichverteilt, innere Schilder werden nicht bevorzugt!) eins der 64 Felder in seinem Arbeitsbereich. Ist das Feld leer, Wiese, Schnee, oder ein Ressourcenvorkommen, welches von dieser Mine nicht gefördert wird, so macht der Minenarbeiter eine 'Leerfahrt' (fördert keine Ressource). Wenn er allerdings ein Schild der richtigen Ressource findet, betrachtet er den Füllgrad. Beträgt dieser >=4, so fördert er eine Ressource. Beträgt der Füllgrad 3, so fördert er zu 75% eine Ressource, zu 25% macht er eine Leerfahrt. Beträgt der Füllgrad 2, so fördert er zu 50% eine Ressource, zu 50% macht er eine Leerfahrt. Beträgt der Füllgrad 1, so fördert er zu 25% eine Ressource, zu 75% macht er eine Leerfahrt. 

Das bedeutet, dass die anfängliche Effizienz einer Mine auf 2er Schildern (-> Füllgrad 6 bis 10) exakt gleich gut ist, wie eine Mine auf 3er Schildern; allerdings fällt der Füllgrad der 2er Schilder natürlich schneller auf unter 4, weshalb die 2er Mine schneller an Effizienz verliert, als die 3er Mine.&#x20;

**6.** Der 'Effizienzbalken' gibt nur den temporären Erfolg der letzten 15 Minengänge an. Das bedeutet, dass selbst eine 10% Mine zeitweise einen 100% grünen Balken haben kann und eine 90% Mine zeitweise einen 0% Balken, wenn der Minenarbeiter bei den letzten 15 Mal suchen überdurschnittlich Glück oder Pech hatte. Dieser Anzeige solltet ihr einfach nicht allzu viel Beachtung schenken. (credits an @Rob | ZL-Primer_S4)&#x20;

**7.** Kombiniert man die Vorkommen aus _3._ mit dem Arbeitsbereich aus _4._ kommt man auf die folgenden optimalen Minenplatzierungen. Für ein Goldvorkommen gibt es 19 Felder (die grünen Baupunkte), um dieses mit einer Mine vollständig zu bearbeiten. Eine Eisen-, Stein- oder Schwefelmine hat 11 solche Felder und eine Kohlemine hat genau 1 solches Feld. Die folgende Grafik gibt grob an, wie viel Effizienzeinbußen man je nach Minenplatzierung macht. 

**Faustregel:** Nehmt immer einen Baupunkt, auf dem auch ein Goldschildchen steht für eure Goldmine.

<figure><img src="https://media.discordapp.net/attachments/576807103256068102/855054461772234772/mineplacement.jpg?width=267\&height=300" alt="Bild"><figcaption>Bild</figcaption></figure>



