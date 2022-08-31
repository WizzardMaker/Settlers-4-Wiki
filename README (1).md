# Baustellenpriorität

{% embed url="https://youtu.be/Gt26_eF8EB8" %}

Ihr habt in Siedler IV die Möglichkeit einzelne Gebäude mithilfe des Prio Buttons auf eine Art bevorzugte Prioritätsliste zu setzen. Doch was genau bedeutet dies für eure Siedlung, und wie kann man mit diesem System arbeiten?

Zuerst müssen wir uns jedoch ansehen, wie Baustellen in Siedler IV abgearbeitet werden. Es gibt für die verschiedensten Sachen in Siedler sogenannte Queues - sprich Listen an Aufgaben die abgearbeitet werden sollen.&#x20;

## Der normale Ablauf einer Baustelle

Wenn ihr nun ein Gebäude setzt, wird dabei wie folgt vorgegangen:

1. Es wird ein Auftrag in die Planiererqueue gepackt, das die neue Baustelle planiert werden soll
2. Herumstehende "Freie" Planierer nehmen diesen Auftrag an und begeben sich zu der Baustelle um mit ihrer Arbeit anzufangen. \
   \-> Wenn eure einzigen freien Planierer am anderen Ende eurer Siedler sind, laufen die Planierer auch durchaus erstmal einige Minuten, bevor sie am Gebäude ankommen. Selbst wenn direkt neben der neuen Baustelle, kurz nachdem die angeforderten Planierer loslaufen, neue Planierer frei werden, übernehmen diese den Job von den bereits angeforderten Planierern nicht.&#x20;
3. Ab einem gewissen Planierungsgrad fordert die Baustelle nun ihre Rohstoffe an, die sie für die Errichtung benötigt. Hierbei werden jedoch maximal 8 Rohstoffe von jeder Ressource auf einmal angefordert.\
   \-> Gebäude die mehr als 8 Rohstoffe eines Typs verlangen, müssen daher zweimal diese Rohstoffe anfordern. Daher dauert beispielsweise die Errichtung von großen Wohnhäusern überhaupt so lange.
4. Ein freier Träger schnappt sich euren Auftrag und bringt eine Ressource zur Baustelle. \
   \-> Bevorzugt werden hier Träger/Rohstoffe genommen, die nah an der Baustelle sind. Daher ist es durchaus ratsam neue Wohnhäuser zwischen alten abgerissen zu errichten, da diese Rohstoffe quasi direkt für die neuen verwendet werden können.&#x20;
5. Sobald die erste Ressource an eurer Baustelle ist, wird ein neuer Auftrag für die Bauarbeiter erstellt. Ähnlich wie bei den Planierern nehmen nun freie Bauarbeiter diesen Auftrag an. \
   \-> Die Reihenfolge der Aufträge spielt hierbei für die Bauarbeiter/Planierer keine Rolle welchen Sie zuerst annehmen. Es wird hierbei lediglich der am wenigsten entferne Bauplatz bevorzugt.&#x20;
6. Eure Baustelle gibt Bauarbeiter wieder frei, wenn keine Rohstoffe mehr dran liegen. Entweder ist die Baustelle dann fertig, oder muss noch mit weiteren beliefert werden. Eure Bauarbeiter können jedoch dann wieder einen anderen Auftrag abarbeiten, wodurch sie sich im Zweifel auch von dem dringend benötigtem Wohnhaus wieder weg bewegen.&#x20;

Das ganze ist etwas vereinfacht dargestellt - und das Verhalten der "Queues" unterscheidet sich auch, ob man mit [Transport+/Kohlefix](multiplayer/transport+-kohlebug-fix.md) oder ohne spielt.&#x20;

## Wo kommt der Priobutton ins Spiel?

Nun - wenn ihr alle Gebäude die im Bau sind permanent auf Prio habt, ist das verhalten identisch zum normalen Ablauf. Aber wenn ihr einzelne Gebäude mit Prio markiert, ändern dies das verhalten für alle anderen Gebäude, die nicht mit Prio markiert sind. \
\-> Das bedeutet aber auch, das Siedler hier die Reihenfolge wie ihr die Priorität verteilt komplett ignoriert, und eher nach dem Prinzip arbeitet welche Priobaustelle in der Nähe ist bei der Annahme einer Aufgabe durch Planierer/Bauarbeiter & Träger.&#x20;

Sobald ihr ein Gebäude mit Priorität belegt habt, ändert sich vor allem das Verhalten der Träger, die das Baumaterial zu der Baustelle bringen soll. **Diese ignorieren ab jetzt alle Baustellen, die keine Priorität haben.**\
\->**Gebäude ohne Prio werden nun also vorerst nicht mehr mit Baustoffen beliefert**. Erst wenn alle Priobaustellen mit einem Typ vom Rohstoff bedient sind (Sprich alles liegt an der Baustelle), wird dieser Baustoff auch auf andere normale Baustellen verteilt. \
Hierdurch werden kurzfristig deutlich weniger Träger die Aufträge abarbeiten müssen. Wenn ihr also in einem (kleinem) Siedlermangel seit, könnt ihr so ein wenig Tricksen um wieder freie Träger zu kriegen.&#x20;

Dieses Verhalten kann sich Beispielsweise der Wikinger zu nutze machen. Indem er seine Holzindustrie mit Prio belegt beim Ausbau, werden so alle anderen Baustellen schon mit Steinen beliefert. (Seine Holzfäller und Förster benötigen lediglich Bretter)

## Vorteile des Priobuttons

Die anderen Queues für Planierer und Bauarbeiter verhalten sich hier ähnlich. Diese bevorzugen zwar priorisierte Gebäude nun, arbeiten aber wenn sie nichts zu tun haben auch die Aufträge von nicht priorisierten Gebäuden ab. \
Dies machen sich daher einige gute Spieler zu nutze, um gezielt ihre Planierer zu steuern und Gebäude vorzuplanieren, bevor sie überhaupt gebraucht werden. So können herumstehende Planierer gezielt schon die ersten Getreidefarmen planieren, während eure Träger lediglich Holz und Stein zu euren priorisierten Gebäuden liefern (wie z.b. weitere Holzfäller, Eisenschmelze oder ähnliches)

Diese Benutzung des Prio Buttons erfordert jedoch einiges an Mehraufwand, und geht immer mit dem Risiko daher das man sich einmal verklickt. So bringen euch dutzend vorplanierte Gebäude nichts, wenn ihr vergesst im rechtzeitigen Moment diese mit in die Prioliste zu packen, sodass diese rechtzeitig gebaut werden.&#x20;

**Es ist also ein schmaler grad zwischen Risiko & Nutzen, den jeder Spieler für sich selber abwägen muss.** \
