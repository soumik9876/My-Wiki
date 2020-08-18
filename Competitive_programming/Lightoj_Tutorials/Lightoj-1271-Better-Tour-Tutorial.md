Author: Soumik Roy<br>
<b>**Hint</b>: This is a bfs problem. In order to keep the path lexicographically smallest,you have to take the smaller node first while traversing.<br>

<b>Detailed tutorial:</b> This is simple bfs. There are only two extra stuffs to do. Printing the path and keeping the path lexicographically smallest.<br>
In order to keep the path lexicographically smallest,we can just sort the child nodes of every node we visit and run a bfs. <br><br>
In order to trace the path,we can have an array/vector which will store the previous/parent node of current index. Before pushing a node to the queue,we can set it's parent node. Finally,we can trace the path by tracking the previous node starting from the ending node until we find the starting node. <br><br>

Consider this case: <br>
6<br>

1 2 3 4 1 3<br>

This graph here:<br>
1->2,4,3<br>
2->1,3<br>
3->2,4<br>
4->3,1<br>

Bfs starts from node 1. We sort the child nodes. While pushing 2 and 3,we set parent of 2 and 3 as 1. We return the bfs when we find 3. We start tracing previous nodes and 
find 3,1. Printing it in reverse order gives the output.

[Solution Link](https://github.com/soumik9876/Lightoj-solutions/blob/master/Lightoj%201271%20-%20Better%20Tour.cpp)
