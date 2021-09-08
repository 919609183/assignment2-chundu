# assignment2-chundu
# AVINASH
###### OOTY

 > Ooty is a town and a municipality in the Nilgiris district of the Indian state of Tamil Nadu. <br> It is located 86 km north west of Coimbatore and 128 km south of Mysore and is the headquarters of the Nilgiris district. It is a popular hill station located in the Nilgiri Hills. It is called Queen of **Western Ghats**. It was the summer capital of Madras Presidency. Originally occupied by the Badaga people and Toda people, the area came under the rule of the East India Company at the end of the 18th century. The economy is based on tourism and agriculture, along with the **manufacture of medicines and photographic film.** The town is connected by the Nilgiri ghat roads and **Nilgiri Mountain Railway**. It's natural environment attracts tourists and it is a popular summer destination.This are the places i like to view in ooty Botanical Gardens, Doddabetta Peak, Ooty Lake, Mudumalai National Park, Avalanche Lake, Government Rose Gardens.

 -----

 Ooty is a year-round destination, but the ideal time to visit is between the months of April to June and September to November and July to September.

 ## Heading for access to reach in order list and unorder list
 1. Start from marryville
 2. Kansas City Airport
    1. chicago Airport
    2. Abu Dhabi
    3. delhi
    4. chennai tamil nadu
3. route map for ooty
 1. Road trip
    2. Chennai to Ooty
    3. Continue to Sastri Nagar
    4. Sastri Nagar to Villupuram
    5. Villupuram to Trichy
    6. Trichy to Kanyakumari
    7. Kanyakumari to Ooty Tamil Nadu, India
 * Items to carry for  Ooty
    * Wallet
    * cards and adress proof's
    * DSLR camera
    * Hoddie
    * clothes
        * woolen shirts
        * jacket
        * caps
    * shoes
    * food packets

**[LinktoAboutMe.md](AboutMe.md)**

------
# Heading for the  creating a Table foods and drinks

**Introduction:**
 The following is to create a table with atleast 4 food/drinks that you would recommend someone try. Include a short paragraph that introduces the table.

|Mandatory   |fav1            |fav2             |fav3             |fav4            |
|:--------:  |:---------:     |:---------:      |:----------:     |:----------:    |
|Food        |biryani         |parota           |mutton           |manshion house  |
|Location    |guntur          |pedakurapadu     |Home             |station         |
|Amount      |300             |60               |700              |1200            |

-----

# Section of Quotes
>“Calm mind brings inner strength and self-confidence, so that’s very important for good health.” 
>**Author:** *Dalai Lama*<br>
>“Being deeply loved by someone gives you strength while loving someone deeply gives you courage.” 
>**Author:** *Lao Tzu*

-----

# create a new section about code fencing
>Unlike tree traversal, graph traversal may require that some vertices be visited more than once, since it is not necessarily known before transitioning to a vertex that it has already been explored. As graphs become more dense, this redundancy becomes more prevalent, causing computation time to increase; as graphs become more sparse, the opposite holds true.

Thus, it is usually necessary to remember which vertices have already been explored by the algorithm, so that vertices are revisited as infrequently as possible (or in the worst case, to prevent the traversal from continuing indefinitely). This may be accomplished by associating each vertex of the graph with a "color" or "visitation" state during the traversal, which is then checked and updated as the algorithm visits each vertex. If the vertex has already been visited, it is ignored and the path is pursued no further; otherwise, the algorithm checks/updates the vertex and continues down its current path. <https://en.wikipedia.org/wiki/Graph_traversal>
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

if (!used[u]) {
    cout << "No path!";
} else {
    vector<int> path;
    for (int v = u; v != -1; v = p[v])
        path.push_back(v);
    reverse(path.begin(), path.end());
    cout << "Path: ";
    for (int v : path)
        cout << v << " ";
}
```
link to the code<https://cp-algorithms.com/graph/breadth-first-search.html>