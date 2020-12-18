# aisports-bomberman
Our solution to the AISports Bomberman Challenge.

In a nutshell: it assigns rewards & costs to both moving & bombing a certain tile. It then moves towards the tile with highest reward/cost

Rewards are based on score that we can obtain and if it can trap/kill an enemy. Finding spots to kill/trap an enemy is similar to looking for articulation points in a graph and that can be done rather efficiently. After that, we scan all these spots and see if we can effectively trap the enemy and reach it earlier.

Costs are based on distances (we used the floyd-warshall algorithm to calculate distances between each pair of tiles on the map) and whether or not we can reach it first. We also have "danger" costs when it is in the splash zone of bombs that are going to explode soon.

**Note:** the code is a huge mess, it's a single file with 1000+ lines of code. I am sorry for that. I will maybe try to clean it up, but that would be quite a lot of work. I think a write-up would be more useful than cleaned up code :).
