# Buildsite priority

Settlers IV offers players the ability to put individual buildings on a priority queue. Understanding the implications of this ability requires knowledge on how a build site normally operates.

## Regular build site operations

If a building is placed, the game does the following:

1. A new request is added to the digger queue.
2. Idle diggers accept this assignment and move to the build suite to start digging.\
   \-> If the only idle diggers are on the other side of the settlement, it can take several minutes for them to arrive. Even if diggers next to this build site finish their tasks, they will not take over the assignment from the other diggers who are en route.
3. Once digging on the build site reaches a certain point, it begins to request the required materials. Only 8 units of each resource can be requested at once.\
   \-> As a result of this behaviour, buildings that require more than 8 resources of one type must request new materials at least twice. This is a major factor in the long build times of large residences.
4. An idle carrier accepts the assignment to carry a resource to the build site, grabs an unused resource and carries it there.\
   \-> The game priorizites resources and carriers who are already near the build site. Therefore, it is advisable to build new residences between old ones that were just demolished by the player. Additionally, this can drastically reduce the amount of digging required, or even skip that step entirely if the player is thorough enough.
5. Once the first piece of building material reaches the build site, a new assignment is created for the builders. Idle builders will accept this assignment in a similar fashion to diggers earlier.\
   \-> The order in which buildings are placed has no bearing on the order in which diggers/builders who finish their current assignment will work on pending build sites. The closest build site is prioritized.
6. The build site will release it's builders once there are no more resources at the build site. Either because the building is finished or because more materials are needed. This can result in breaks during which builders might move away from more important build sites.

This is a simplified explanation. Queue behavior is also affected if [Transport+/Coalfix](../multiplayer/transport+-kohlebug-fix.md) is activated.&#x20;

## How does the priority button change this?

If all build sites are set to high priority, the behavior remains the same. But if individual buildings are tagged as high priority, this alters the behavior for all buildings which do not share that setting.\
\-> This also means that the order in which build orders were given is completely ignored.

Once a building has been marked with high priority, **carriers will ignore all build sites that are not set to priority. Thus, they will not be supplied with materials until all prioritized build sites have had their materials delivered to them.** \
This can be used to mitigate a small settler shortage, as there won't be as many requests for carriers to work through.&#x20;

In another example, a viking player can use this behavior by assigning priority to their wood production buildings, allowing all other build sites to have stone delivered to them in advance since woodcutters and foresters don't require any stone.&#x20;

## Advantages of priority queue

The other queues for builders and diggers act similarly. They now prefer prioritized buildings, but will work on the other buildings if they would otherwise be idle.

Some players use this to micromanage their diggers and pre-dig buildings in advance. For example, idle diggers can start working on the first grain farms while carriers will only supply prioritized buildings with materials.&#x20;

Using priority in this manner requires additional micromanaging and increases the possibility of human error. A dozen pre-dug buildings are useless if they aren't set to priority at the right moment so they are actually built on time.&#x20;

**Therefore, the priority button is very much a double-edged sword. Whether or not to use it is a decision each player needs to make for themselves.**&#x20;
