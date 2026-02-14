Graph based Inelligent Traffic Routing for Universirty Network

Input;
 Network devices (routers,switches,labs,servers)
 Physical Network connections 
 Traffic load and Delay vlaues for each connection link
 Source node
 Destination node


Output;
 Getting the best internal network path with minimum traffic 



Step by step Algorithm;
 
  Creating a weighted graph A
  Representing each network device as Vertex
  Representing each network link as Edge
  Assign weights based on traffic load or delay
  Store the GRAPH using Adjacency lis
  Mark the Source node distance as 0
  Mark all the other node distances as infinity
  Select the non visited node with the minimum distance
  Update the current distance to the neighboring nodes
  Repeat the process until destination is reached
  Select the path with the minimum final weight
  Route the traffic through the choosen path
  Update the edge weights automatically during traffic


Complexity Analysis;

  Space complexity : O(V+E)
  Time complexity : O(E log V)


Pseudo Codes;

BEGIN

  CREATE Graph A
  A contains:
        Vertices = network devices 
                   (routers,switches,labs,servers)

  Edges = network links between devices
  Weights = traffic load or delay on each link


  for each vertex v in G do
        distance[v] = INFINITY
        visited[v] = FALSE
  end for

  distance[source] =- 0


  while non visited vertices avaliable do

  u = vertex with minimum distance value
      visited[u] = True

  for each neighbor n of u do
  if visited[n] = false do
                newpath = distance[u] + weight(u, n)

  if newpath < distance[n] then
                    distance[n] = newpath
                    head[n] = u
                end if
            end if
        end for
    end while

  bestPath = trace path from destination to source using head[]

  SEND network traffic through bestPath

  if traffic load increases on any link then
        UPDATE corresponding edge weight
        REPEAT routing algorithm
    end if

end


