---
description: by Phottor
---

# Effects of Fighting Strength

## Explanation

Whenever a unit attacks, it's base damage value is multiplied by the player's fighting strength, potentially doubled and/or halved by spells like bloodrush or shield, and reduced by the target's armor (if it is a squad leader).

The resulting damage value is deducted from the target's hitpoints. If those are reduced to or below 0, the unit dies. If the attacking unit is on it's own or allied territory, defensive fighting strength applies. If it is on hostile or neutral territory, the offensive fighting strength applies.

The resulting damage value is rounded to the nearest full integer, although the game appears to start rounding up at x.48 rather than x.5.&#x20;

A unit can only have, gain or lose a natural number of health points. This rounding behavior results in certain threshholds were an increase in fighting strength increases damage by one point.

For example, a level 3 swordsman deals 20 damage at 100% fighting strength. At 102, that increases to 20.4 = 20. At 103, we get 20.6=21. Thes threshhold were a damage increases decreases the amount of attacks needed to kill an enemy unit is called a **KK-Tick** (Fighting Strength Tick) or a **Spike**.

For example, a Level 3 swordsman dealing 21 or 22 damage needs 10 hits to kill an enemy unit of the same type in either case. In a pure swordsmen army, both would effectively be on equal footing.

## **Fighting Strength Ticks of L3 units**

These are the FS-Ticks complied for the most important army constellations.

_1. Column FS Spikes_ \
_2. Column Hits per Kill_&#x20;

{% tabs %}
{% tab title="Swords FS vs. Swords" %}
**Swords FS vs. Swords**

`25 - 28 - 33 - 38 - 43 - 48 - 53 - 58 - 63 - 68 - 73 - 83 - 88 - 98 - 103 - 118 - 133 - 148`

`42 - 35 - 30 - 27 - 24 - 21 - 20 - 18 - 17 - 15 - 14 - 13 - 12 - 11 - 10  - 9   - 8   - 7`
{% endtab %}

{% tab title="Swords FS vs. Archers" %}
**Swords FS vs. Archers**

`25 - 28 - 33 - 38 - 43 - 48 - 53 - 58 - 63 - 68 - 73 - 78 - 88 - 98 - 113 - 133`

`32 - 27 - 23 - 20 - 18 - 16 - 15 - 14 - 13 - 12 - 11 - 10 - 9  - 8  - 7   - 6`
{% endtab %}

{% tab title="Archer FS vs. Archers" %}
**Archer FS vs. Archers (spikes are the same against all other units**

`25 - 32 - 44 - 57 - 69 - 81 - 94 - 106 - 119 - 131 - 144`

`80 - 54 - 40 - 32 - 27 - 23 - 20 - 18  - 16  - 15  - 14`
{% endtab %}
{% endtabs %}

The hits per kill indicate that archers gain about 11% in terms of strength when making the jump from 106 to 119 fighting strength, while the jump from 119 to 132 only equals an increase about 6%. This should be kept in mind when noting that a player has an addition FS Spike compared to another.

## FS Table of all units

This table contains all the FS-Spikes for all non-special units. Do note that due to the odd rounding as noted above, some of these values are off by one point.

![by Nightfever221](../.gitbook/assets/table.png)

## FS Table for special units (not yet available)

There is no table yet for the other units. It is relatively easy to calculate the FS spikes for special units.&#x20;

For example, a level 3 backpack catapultist has 13 base damage. 1/13 = 0.0769... = 7,69FS are needed to increase his damage by one point. The game rounds up at the halfway point, so the first spike after 100 FS ist at 103.84=104 FS.

After that, the spikes continue in 7.69 FS intervals. Backpack catapultists also have the unique property of dealing AoE damage, making it difficult to clearly calculate the amount of hits needed for each kill. Some spikes also increase the amount of damage dealt in one or both of the AoE radii.

**As a rule of thumb: The more damage, the better.**
