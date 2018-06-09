# Dijkstra Algorithm using Data Structure in C

Implementing a solution for the shortest path problem using Dijkstra algorithm

## Condition
a.The node of the graph is not going to be more than 20.

b.The names of the nodes are Englishalphabets (Uppercase) like A,B,...

c.The distance between two nodes is greater than Zero.

d.Use 3200 as the infinity number.

## Getting Input
It assumes these input below
~~~
int getNumberOfNodes()
{ 
    return 6;
}
int getNumberOfEdges()
{ 
    return 9; 
}
char* getNodes()
{ 
    return "A,B,C,D,E,F,G"; //these are the nodes of the graph!
}
char* getEdges()
{ 
    return "A_B_1,A_C_2,B_C_4,B_D_5,C_E_3,D_E_2,D_F_4,E_B_2,E_F_6"; 
}
~~~

![ImgDijkstra](https://i.imgur.com/6EMAgYF.jpg)

## Defining Structure
~~~
struct Edge
{
    int distance;
    struct Node *to;
    struct Edge *next;
};

struct Node
{
    int visited;
    char name;
    int cost;
    struct Node *from;
    struct Edge *edge;
    struct Node *next;
};
~~~

### struct Node

![structure-Node](https://i.imgur.com/hsVG1NN.jpg)


![structure-Node-next](https://i.imgur.com/YWC1VW7.jpg)

### struct Edge

![structure-Edge](https://i.imgur.com/kBzf6Dg.jpg)
