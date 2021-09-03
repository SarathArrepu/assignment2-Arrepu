# Assignment2-Arrepu
# Sarath Arrepu

###### City - venice/ Country - Iceland


 Venice, known also as the “City of Canals,” “The Floating City,” and “Serenissima,” is arguably one of **Italy’s most picturesque cities. With its winding canals, striking architecture, and beautiful bridges**, Venice is a popular destination for travel.

 Iceland, island country located in the North Atlantic Ocean. Lying on the constantly active geologic border between North America and Europe, **Iceland is a land of vivid contrasts of climate, geography, and culture**. Sparkling glaciers, such as Vatna Glacier (Vatnajökull), Europe’s largest, lie across its ruggedly beautiful mountain ranges; abundant hot geysers provide heat for many of the country’s homes and buildings and allow for hothouse agriculture year-round; and the offshore Gulf Stream provides a surprisingly mild climate for what is one of the northernmost inhabited places on the planet.

---  
# Directions to Statue of Liberty from Maryville  
1. Take a cab to Kansas airport from Maryville.
    1. Book cab in Uber/Tap ride.
    2. book your ticket to new york.
2. Once you land in New york
    1. Book a cab to NY 10004.
    2. Take a ferry and reach the monument.
3. Take a seflie and post.

---
# Items to carry(unordered)
* Cellphone is most important 
* Camera
  * lens
  * tripod stand
 

# About ME
[ClickHere](https://github.com/SarathArrepu/assignment2-Arrepu/blob/main/AboutME.md)


---------
# **FOOD RECOMMEDATIONS**
#### The below table has the food recommedations in maryville city. My personal choice would be pizza which is available in pizza hut located opposite to shell petrol , orange juice at macey's is simply amazing which is made of fresh pulp and adundant in vitamin c. For dinner white sauce pasta at A&G is just mouth watering its the chef's recommdation. I would suggest everyone to try these.

|Food/Drinks|location |price|
|-----------|---------|-----|
| pizza     |pizza hut|$12.2| 
|Orangejuice| Maceys  |$2   |
| pasta     | A & G   |$15.1|

---
# **QUOTES**
> “Be yourself; everyone else is already taken.” 
***Oscar Wilde***.

> “Two things are infinite: the universe and human stupidity; and I'm not sure about the universe.”
***Albert Einstein***.

-----------
# Code Fencing - Graphs Traversal/connected/shortest paths

> The algorithm takes as input an unweighted graph and the id of the source vertex s. The input graph can be directed or undirected, it does not matter to the algorithm.
The algorithm can be understood as a fire spreading on the graph: at the zeroth step only the source s is on fire. At each step, the fire burning at each vertex spreads to all of its neighbors. In one iteration of the algorithm, the "ring of fire" is expanded in width by one unit (hence the name of the algorithm).
More precisely, the algorithm can be stated as follows: Create a queue q which will contain the vertices to be processed and a Boolean array used[] which indicates for each vertex, if it has been lit (or visited) or not.
Initially, push the source s to the queue and set used[s]=true, and for all other vertices v set used[v]=false. Then, loop until the queue is empty and in each iteration, pop a vertex from the front of the queue. Iterate through all the edges going out of this vertex and if some of these edges go to vertices that are not already lit, set them on fire and place them in the queue.

[ForMoreinfomation](https://cp-algorithms.com/index.html)

```
vector<vector<int>> adj;  // adjacency list representation
int n; // number of nodes
int s; // source vertex

queue<int> q;
vector<bool> used(n);
vector<int> d(n), p(n);

q.push(s);
used[s] = true;
p[s] = -1;
while (!q.empty()) {
    int v = q.front();
    q.pop();
    for (int u : adj[v]) {
        if (!used[u]) {
            used[u] = true;
            q.push(u);
            d[u] = d[v] + 1;
            p[u] = v;
        }
    }
}

```
[ForMoreinfomation_SourceCode](https://cp-algorithms.com/graph/breadth-first-search.html)