Download Link: https://assignmentchef.com/product/solved-ada-mini-homework-2
<br>
<h1>To DFS, or to BFS, that is the question</h1>

<h2>Problem Description</h2>

<em>TL; DR: Given a connected graph with N vertices and M bidirectional edges, please output the lexicographically smallest DFS sequence and the lexicographically smallest BFS sequence.</em>

<em>BB Travel Inc.</em>, a traveling agency in the <em>ADA Kingdom</em>, would like to launch a tourist plan that visit every city in the kingdom. The <em>ADA Kingdom </em>consists of <em>N </em>cities number from 1 to <em>N</em>, where the city numbered 1 is the capital. There are also <em>M </em><strong>bidirectional </strong>road connecting pairs of cities. You can reach any city from any city using some of the roads.

The tourist plan should be a valid <strong>Depth-First Search (DFS) </strong>or <strong>Breadth-First Search (BFS) </strong>sequence of the kingdom starting from the capital (city 1). Thus, it should be a sequence of cities <em>s</em><sub>1</sub><em>,s</em><sub>2</sub><em>,…,s<sub>N</sub></em>, where <em>s</em><sub>1 </sub>= 1, and each city occurs exactly once. Additionally, to attract more customers, the plan should be as <em>attractive </em>as possible. We say plan <em>s </em>is more <em>attractive </em>than plan <em>s</em><sup>′</sup>, if <em>s </em>is <strong>lexicographically smaller </strong>than <em>s</em><sup>′</sup>.

Since <em>BB Travel Inc. </em>doesn’t know whether their customers prefer BFS order or DFS order yet, they ask you to help them find out the plan for both scenarios (i.e. one plan for DFS, and one plan for BFS).

<h2>Glossary</h2>

Please see the course slides for the definition of <em>Depth-First Search </em>and <em>Breadth-First Search</em>. Note that for the case of <em>BFS</em>, the order is valid as long as we choose an unvisited vertex closest to the starting vertex every time.

A valid DFS/BFS sequence is a sequence <em>s</em>, such that there exists a DFS/BFS search order, where <em>s<sub>i </sub></em>is the <em>i</em>-th vertex added into the DFS/BFS tree.

A sequence <em>s </em>is <em>lexicographically smaller </em>than <em>s</em><sup>′ </sup>if there exists a index <em>t</em>, such that and <em>s<sub>t </sub>&lt; s</em><sup>′</sup><em><sub>t</sub></em>.

<h2>Input</h2>

The first line of the input contains two integers <em>N </em>and <em>M</em>, denoting the number of cities and the number of roads in the <em>ADA Kingdom</em>.

The next <em>M </em>lines describes the roads connecting the cities. The <em>i</em>-th line contains two integers <em>u<sub>i </sub></em>and <em>v<sub>i</sub></em>, denoting a bidirectional road connecting city <em>u<sub>i </sub></em>and <em>v<sub>i</sub></em>.

<ul>

 <li>1 ≤ <em>N </em>≤ 10<sup>5</sup></li>

 <li>1 ≤ <em>M </em>≤ 2 × 10<sup>5</sup></li>

 <li>1 ≤ <em>u<sub>i</sub>,v<sub>i </sub></em>≤ <em>N,</em>∀1 ≤ <em>i </em>≤ <em>M</em></li>

 <li><em>u<sub>i </sub></em≯= <em>v<sub>i</sub>,</em>∀1 ≤ <em>i </em>≤ <em>M</em></li>

 <li>You can reach any city from any city using some of the roads.</li>

 <li>Every pair of cities is directly connected by at most one edge.</li>

</ul>




<strong>Test Group 0 (0 %)</strong>

<ul>

 <li>Sample Input</li>

</ul>

<strong>Test Group 2 (75 %)</strong>

<ul>

 <li>No Additional Constraint <strong>Output</strong></li>

</ul>

<strong>Test Group 1 (25 %)</strong>

<ul>

 <li><em>N </em>≤ 1000</li>

 <li><em>M </em>≤ 2000</li>

</ul>




Please output two lines. The first line contains the most <em>attractive </em><strong>DFS </strong>trip plan starting from the capital. The second line contains the most <em>attractive </em><strong>BFS </strong>trip plan starting from the capital.

<strong>Sample Input 1                                                        Sample Input 2</strong>

5 7

5 4

5 4

1 2

3 5

<ul>

 <li>4</li>

 <li>3</li>

 <li>3</li>

 <li>1</li>

 <li>5</li>

</ul>

1 4

<ul>

 <li>4</li>

 <li>2</li>

</ul>

<strong>Sample Output 1</strong>

<strong>Sample Output 2</strong>

1 2 5 4 3                                                                                               1 4 2 3 5

1 2 4 3 5                                                                                               1 4 5 2 3

<h2>Hint</h2>

<ol>

 <li>bidirectional = undirected ̸= unidirectional</li>

 <li>Make sure you understand the sample input/outputs before coding.</li>

 <li>STL is your good firend. For example:

  <ul>

   <li>You can use std::vector to store the graph (adjacency list).</li>

   <li>You can use std::sort to sort an array/vector/etc.</li>

  </ul></li>

</ol>