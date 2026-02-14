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
 
  1. Creating a weighted graph A
  2. Representing each network device as Vertex
  3. Representing each network link as Edge
  4. Assign weights based on traffic load or delay
  5. Store the GRAPH using Adjacency lis
  6. Mark the Source node distance as 0
  7. Mark all the other node distances as infinity
  8. Select the non visited node with the minimum distance
  9. Update the current distance to the neighboring nodes
  10. Repeat the process until destination is reached
  11. Select the path with the minimum final weight
  12. Route the traffic through the choosen path
  13. Update the edge weights automatically during traffic


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


