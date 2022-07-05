---
description: by Phottor
---

# Fighting strength calculationg

## Overview

{% embed url="https://www.youtube.com/watch?v=YcVu_iQ8FAo" %}
Video by [UltimateSpinDash](https://www.youtube.com/channel/UCXRXmtOKDS3iX2QJDCffwLA)
{% endembed %}



## Factors in offensive fighting strength

Offensive fighting strength is determined by the following factors:

* Player count (determines the starting value)
* Resources used in buildings
* Amount of finished eyecatcher-sets - a set referring to all 12 eyecatchers being built once.

## **Formula**

`ATK = (256*(STONE + WOOD + 2*GOLD + 3*EYECATCHERSTONE + 3*EYECATCHERWOOD + 6*EYECATCHERGOLD )+127)//1000 + START + EYECATCHERSETS*30`

`FS = ATK*100//256`

STONE, WOOD, GOLD = resources used in regular buildings\
EYECATCHERTSTONE, EYECATCHERWOOD, EYECATCHERGOLD = resources used in eyecatchers\
START = Starting value determined by player count\
EYECATCHERSETS = Amount of completed eyecatcher sets

### **Resource values**

* 1 piece of wood or stone is worth 1 resource
* 1 piece of gold (in practice, only in temples) is worth 2 resources
* 1 piece of wood or stone spent on eyecatchers is worth 3 resources.
* 1 piece of gold spent on eyecatchers is worth 6 resources.
* 1 full set of eyecatchers grants an additional bonus of about 117 extra resources.

### **Resource requirements**

A full set of eyecatchers has the following requirements for each civilization:

* \[R] : 18H 40S 26G = 330 resources
* \[W] : 24H 23S 27G = 303 resources
* \[M] : 9H 56S 30G = 375 resources
* \[T] : 17H 46S 31G = 375 resources

In addition to the set bonus of 117 resources.

### Fighting Strength Threshholds

The formula has several break points where the amount of points that is used for Fighting Strength is halved. This results in diminishing returns as fighting strength increases. These break points are at 50, 100 and 125 offensive fighting strength, or the equivalent ATK values, 128, 256, 320.

* \[25, 50] : All resources count fully towards fighting strength
* \[51, 100] : All additional resources at this point add 50% of their base value to fighting strength.
* \[101, 125] : All additional resources at this point add 25% of their base value to fighting strength.
* \[126, 150] : All additional resources at this point add 12.5% of their base value to fighting strength.

Internally, the game runs the following checks in the order listed:

* if ATK > 128, then ATK = 128 + (ATK-128)//2
* if ATK > 256, then ATK = 256 + (ATK-256)//2
* if ATK > 320, then ATK = 320 + (ATK-320)//2

### Simplified rule of thumb

The above formula multiplies a resource with 256, divides it by 1000 and then calculcates the final percentage by multiplying by 100 and dividing by 256.

**Conclusion:** 1 resource equals 0,1 percentage points. Combined with the established threshholds, the following amount of resources is needed to increase your fighting strength by 1%.

* \[25, 50] : 10 resources per percentage point
* \[51, 100] : 20 resources per percentage point
* \[101, 125] : 40 resources per percentage point
* \[126, 150] : 80 resources per percentage point

## Starting fighting strength

* 8 : \[25%] (START=64)
* 7 : \[27%] (START=69)
* 6 : \[30%] (START=76)
* 5 : \[33%] (START=85)
* 4 : \[37%] (START=96)
* 3 : \[42%] (START=109)
* 2 : \[50%] (START=128)
* 1 : \[55%] (START=153)&#x20;

The 50% threshhold is already considered for 1 and 2 player starts.

## Defensive fighting strength

Defensive fighting strength is directly tied to offensive fighting strength, but starts at 100%. Once offensive fighting strength surpasses 100%, defensive fighting strength scales at half the speed.
