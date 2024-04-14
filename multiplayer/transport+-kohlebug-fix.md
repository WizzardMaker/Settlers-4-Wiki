# Transport+ / "Coalbug"fix

<iframe style="width: 100%;aspect-ratio:16/9;" src="https://www.youtube.com/embed/NSWV3QzbWQU" frameborder="0" allowfullscreen></iframe>
<figcaption markdown>
Video by [UltimateSpinDash](https://www.youtube.com/channel/UCXRXmtOKDS3iX2QJDCffwLA)

</figcaption>
            

## What is the coalbug?

Settlers III and IV were developed and released at a time when most CPUs clocked in around 500Mhz or even lower. To avoid putting to much stress on this hardware, the developers put a limit on the amount of goods of each type could be requested for various tasks in the settlement simultaneously.&#x20;

Internally, the game works with so called "Ticks" - 14 ticks are processed each second. The original limit saw each good being requested once every 16 ticks. This resulted in up to 52 units of each type that could be requested each minute. Exceptions were made for building materials and coal, which can request twice as many items. This is resulted in what is known as the [HE build](../produktionsverhaeltnisse/he-maximum-buildup-2-1-gold.md), which is optimized to create as many L3 soldiers as possible within these limitations.

## The actual fix

A modder named nyfrk developed a workaround to bypass this artificial limit a couple of years ago. It can be found on [Github ](https://github.com/nyfrk/Settlers4-Coalfix)and is integrated into [Settlers United](settlers-united.md) under the name "Transport+".&#x20;

The fix reduces the timing from 16 ticks down to 1, meaning that all previous limits are increased by 16 times. In theory, up to 1664 coal transport requests are possible each minute.

## Side effects

This fix has several implications. Settlers now react to goods much faster. This is particularly important for barracks, which become much more efficient and can produce soldiers much faster, especially if gold and weapons are readily availabe in a nearby storage.

However, this also means that a lot more settlers are needed in the late game.
