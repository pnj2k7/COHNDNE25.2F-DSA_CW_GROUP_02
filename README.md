Module Information;
    Instituion : NIBM - COL 07
    Course : HNDNE25.2F
    Module : Data Structure and Algorithms
    Assessment Type : Coursework

Group Information;
Name : H M A P N L JAYAWICKRAMA
Student ID : COHNDNE252F-002
Batch : HNDNE 25.2F

Name :  A D T SILVA
Student ID : COHNDNE252F-014
Batch : HNDNE25.2F


Introduction:
This coursework shows a solution for a realistic scenario on a network issue at a university, which runs on LAN (Large Area Network) and this suggests a solution that is based on the GRAPH data-structure to provide intelligent traffic routing.
The solution shows how Data Structures and Algorithms (DSA) concepts can be effectively implemented to a realistic working environment related to network communication.

Networking Scenario:
    The University LAN network connects:
        Academic floors in the building
        Computer Laborataries
        Network Laborataries
        Administrative Offices
        Central Servers
        Wireless Access Points


Identified Problem;
During the peak data transaction periods, such as running heavy downloads, using multiple of laboratories together and large count of LMS access, the network experiences a congention.

Certain internal routes become overloaded and lternative paths remain without being used which will reasult finally to poor network performance.


Problem Statement;
This network lacks an intelligent routing mechanism to dynimaclly distribute internal traffic based on congestions occuring levels and points, which lead to a downfall in network performance and stability.


Propsed Solution;
A Graph based Intelligent Traffic Routing system by selecting "Weighted Graph Data Structure" is propsed as the solution to optimize the internal traffic flow of the network environment by dynamically selecting the least congested internal route to data tranfer in the network system.


Graph Representation:
    Vertices (Nodes)
        Routers
        Switchers
        Academic floor pointers
        Computer and Network labs
        Central Servers


  Edges (Links)
        Fibre Optic cables
        Ethernet connections
    
  Edge Weights
        Network delay
        Traffic load
        Bandwidth usage


Justification for Selection of Graph;
    Network is interconnected with each other endpoints
    Existing od multiple routing paths
    Efficent topology representation
    Congestion aware routing
    Selection of best appropriate path to transfer
    Similar task is done in enterprise routing concept (OSPF)

Simultaion Process;
    Network is transfered as a weighted graph
    Network devices are assigned as nodes
    Connections are assigned as edges
    Higher weights are assigned for the conjested links
    Using Shortest-path logic (Dijkstra) to select least conjested route
    Traffic will be dynimically allocated for the suitable paths during traffic


Algothrithm Concept;
    Shortest path Algorith (Dijkstra)
 
 Ensures a minimum delay in transfer
 Usage of efficent bandwidth
 Balanced traffic flow for the internal environment

Space complexity;
    Measure the sapce allocation of memory for algorithm
        O(V+E)

Every node will consist a mempry for Vertices
Every link will consist a memory for Edges

so, Memory depends of total of no:of nodes and no: of links

Time Complexity:
    Time taken by the algorithm to find the best path
       O(E log V)

Checks for the edges and uses a priority queue to choose from Vertices nodes





