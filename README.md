# CSES

# Introductory problems
Problem|solution|code
--|--|--
[ChessBoard and Queens](https://cses.fi/problemset/task/1624)|Diagnols have constant value. Each right diagnol is (i+j) and each main diagnol is i-j |[code](https://cses.fi/problemset/result/6599898/)
[digit queries](https://cses.fi/problemset/task/2431/)|there are 9 number with 1 length digit, 90 numbers with 2 length digits , 900 (3) digit numbers|[code](https://cses.fi/problemset/result/6557835/)
[Grid paths](https://cses.fi/problemset/task/1625)|A path that forms a loop can't be traversed.(if front and back are visited and left and right not visited then do not traverse the path.)|[code](https://cses.fi/problemset/result/6583420/)


# Dynamic programming
Problem|solution|code
--|--|--
[Dice Combinations](https://cses.fi/problemset/task/1633/)|dp[0]=1(when no dice is thrown). get i as sum from dp[i-diceNum] ways|[code](https://cses.fi/problemset/result/6599986/)
[Minimizing Coins](https://cses.fi/problemset/task/1634)| 10^8 worked on cses, dp[i]=min(dp[i],1+dp[i-coins[i]])|[code](https://cses.fi/problemset/result/6607594/)
[Coin Combinations I](https://cses.fi/problemset/task/1635) | for any no. of combination loop through coins again and again for each sum of money. dp[i]+=dp[i-coins[j]]|[code](https://cses.fi/problemset/result/6607680/)
[Coin Combinations II](https://cses.fi/problemset/task/1636/) | for unique combination traverse each coin once. dp[j]+=dp[j-coins[i]]|[code](https://cses.fi/problemset/result/6607947/)
[Removing digits](https://cses.fi/problemset/task/1637)|always remove max digit|[code](https://cses.fi/problemset/result/6608062/)
[Grid Paths](https://cses.fi/problemset/task/1638)|dp[i][j]=dp[i-1][j]+dp[i][j-1]|[code](https://cses.fi/problemset/result/6608226/)
[Book Shop](https://cses.fi/problemset/task/1158)|0-1 knapsack, dp[i][cost]=max(dp[i-1][cost],dp[i-1][cost-c[i]])|[code](https://cses.fi/problemset/result/6618408/)
[Array Description](https://cses.fi/problemset/task/1746) | if arr[i]=0 new dp[i]=previous dp[i-1]+dp[i]+dp[i+1] else rest dp[i]=0|[code](https://cses.fi/problemset/result/6622730/)
[Counting Towers](https://cses.fi/problemset/task/2413)|for (n,n-1) sub-block it can be considered as 2X2 block which has 8 possible solution.there can be 4 states where transition is from vertical line block -> no line block,vertical line-> vertical line, no line->vertical line, no line-> no line. dp[i][0]=((dp[i-1][0]<<1)+dp[i-1][1])%mod , dp[i][1]=((dp[i-1][1]<<2)+dp[i-1][0])%mod |[code](https://cses.fi/problemset/result/6623117/)
[Edit Distance](https://cses.fi/problemset/task/1639/)|if string is of 0 length the min operation would be the other strings length. dp[i][j]=min(1+dp[i-1][j],1+dp[i][j-1],a[i]==b[j]+dp[i-1][j-1])|[code](https://cses.fi/problemset/result/6643334/)
[Rectangle Cutting](https://cses.fi/problemset/task/1744/)|base case is when square is formed then dp[i][i]=0. here dp[i][j] means iXJ dimensional rectangle and not the not matrix indices.To compute for iXJ rectangle cut the rectangle into two pices column wise then row wise as each smaller cut is already computed, so iXJ can be found out.Its cost is minimum of all sub rectangular division+1|[code](https://cses.fi/problemset/result/6645476/)
[money sums](https://cses.fi/problemset/task/1745)|dp[0]=1 , iterate all coins and for each coin iterate all possible sum and mark that different sum. At last count all marked sum that are possible|[code](https://cses.fi/problemset/result/6647695/)
[Removal Game](https://cses.fi/problemset/task/1097)|If two people are playing alternatively then both person will have different set of digits. let set 1 has total sum of X and set 2 has total sum of Y then X+y= total sum of array. Here we want to find X if both player play optimally. if we get X-Y = T somehow then X can find as X=(totalsum+T)/2. we have array arr[i....j] then if a person choose arr[i] or arr[j] and remove them then it will be max of both choice , then ans=max(arr[i]-dp[i+1...j],arr[j]-dp[i...j-1]). Also a-(b-(c-(d-(e...))))= (a+c+e)-(b+d) .final ans will be the value of X-Y and hence X can be calculated|[code](https://cses.fi/problemset/result/6659104/)
[Two sets II](https://cses.fi/problemset/task/1093)|it is 0-1 knapsack|[code](https://cses.fi/problemset/result/6657156/)
[increasing subsequence](https://cses.fi/problemset/task/1145)|end[i] is the minimum number which ends of longest increasing subsequence having length i+1. end[] is not the final LIS but it stores the least number that are end of lis having length i+1.If a number num is encountered while traversing then it is put at position where length is i+1 and its least there using binary search lower bound , if no such position is found then it is put at the end of end[] array.end[] is always an increasing sequence.|[code](https://cses.fi/problemset/result/6660917/) 
[projects](https://cses.fi/problemset/task/1140)|sort according to the end work day of each project.dp[i] will store the maximum amount of money that can be earned till ith day.dp[i]=max(dp[i-1],lower_bound(start of work day[i])), it is either taking score of the ith day to final answer or not including it to final answer.|[code](https://cses.fi/paste/75817c5aac1af2f765da4a/)
[Elevator Rides](https://cses.fi/problemset/task/1653)| bitmask dp, if dp[100101] is to be calculated then it is result of dp[000101], dp[100001] and dp[1000100]. traverse from 0 to pow(2,n) and larger subset dp can be calculated by removing each bits at a time as subproblems solution is known then the dp can be computed.Here we have to find number of minimum rides for all the people and how much total weight is in the last ride. dp[subsequence]={rides,min_weight at last ride} is calculated by going through each subset from smaller to higher . dp[0]={1,0} , for no people in lift total rides is least 1 and last ride weight in lift is 0 this is the base case.|[code](https://cses.fi/paste/47715dab16859bd865cef9/)
[Counting Tilings](https://cses.fi/problemset/task/2181/)|Thinking brute force way , first find total number of ways to tile first column , then 2nd column and so on.previous Tile can be represented as binary number of max length 10. each valid binary tiling way is find out taking previous tiling way into  consideration. [tiling way for particular column] +=[tiling way for previous column] because if a particular column can be tiled in a way then it has some horizontal tiles then for next column tiles can be placed in only some position then all possible ways of tiling for those positions is found out.At the end we get the answer|[code](https://cses.fi/paste/3055a567d6ac2d85660591/)
[counting numbers](https://cses.fi/problemset/task/2220)|Always apply reccurence solution for digit dynamic programming first , index of array and tight is always there for every digit dp. then other constrainst like sum or previous digit or leading zeros can be added to parameters . if tight is true traversal is bounded till that fixed digit in the number otherwise traversal  is till 9, then recursively solve the problem.convert it to dp & initially all dp states is -1 |[code](https://cses.fi/paste/b245238f42728c9e65f592/)


# Graphs
Problem|solution|code
--|--|--
[Counting Rooms](https://cses.fi/problemset/task/1192)|simple dfs|[code](https://cses.fi/problemset/result/6686876/)
[Labyrinth](https://cses.fi/problemset/task/1193)|track previous path visited (bfs)|[code](https://cses.fi/paste/12f26954efdf021166265a/)
[Building Roads](https://cses.fi/problemset/task/1666)|connect one node from  each non connected sets of graph|[code](https://cses.fi/paste/8718d4c0654b5be9662ea2/)
[Message Route](https://cses.fi/problemset/task/1667)|Store previous node info while bfs|[code](https://cses.fi/paste/971f0de8610c3b856640b3/)
[Round Trip](https://cses.fi/problemset/task/1669)|here we have to find the loop in the undirected graph. Store previous node info(parent) using node and print the loop elements.| [code](https://cses.fi/paste/801370f1f83b034f66ccd0/)
[Monsters](https://cses.fi/problemset/task/1194)|its simple bfs, first process all monsters then player, use simple visited matrix & track previous path followed.|[code](https://cses.fi/paste/d297ff8fa88e0fd666dcf9/)
[Shortest Routes I](https://cses.fi/problemset/task/1671)|Simple dijkstra, but two citys  can have different distance in between them, so process only city's paht that can reach us to another city with bare min distance.|[code](https://cses.fi/paste/17e210f0b4761c0966e415/)
[Shortest Routes II](https://cses.fi/problemset/task/1672)|it's floyd warshall algorithm , for each intermediate city compute shortest distance between two cities.|[code](https://cses.fi/paste/02eb22e3b515ad5466fff5/)
[High Score](https://cses.fi/problemset/task/1673)|mark those nodes that can be visited by starting node ( here starting node is 1).It can have positive cycle which can increase score when cycle is visited again and again to track this cycle bellman ford is applied on nodes which are marked initially. once bellman ford is applied store the score of destination node  and reapply bellman ford on nodes which are marked initially and make new distance as infinite because there will be cycle and positive cycles add upto infinite , at end of this bellmand ford algorithm the end node or destination node may change if the positive cycle affected it's score. if it affects then return -1 else display score.|[code](https://cses.fi/paste/e6b5aaeb18c379366707e5/)
[Flight Discount](https://cses.fi/problemset/task/1195)|Apply dijkstra starting from node 1 such that we get all other distances from node 1.After reversing graph, Apply dijkstra starting from node n such that we get all other distances from node n. Now iterate over all edges and cost =minimum(cost,cost1[a]+weight/2+costn[b]).
[Cycle Finding](https://cses.fi/problemset/task/1197)|apply floyd warshall and also store previous nodes connecting the node. cycle can be O-O like two negative cycles connecting each other and we can not determine using a node if it's inside a cycle or not. To overcome this problem revisit previous node each time n times . after it will be sure that start node is in a negative cycle as there are max n nodes.Then store and display the cycle.|[code](https://cses.fi/paste/f00c78327a690035672d1d/)
[Flight routes](https://cses.fi/problemset/task/1196)|maintain a array of max priority queue for storing distance of best k shortest routes . Perform dijkstra , if size of distance array is less than k then insert the current  distance , else insert more smaller distance and remove bigger distance, size shouldn't exceed k for any priority queue. array[n] will contain the answer.|[code](https://cses.fi/paste/73130aa80f4e70e2674e19/)
[Round Trip II](https://cses.fi/problemset/task/1678)|Don't ever try to store previous state in dfs on graph, I lack understanding and it's very difficult more me.Just Maintain a onStack array if the node is onStack and it's visited then it is the end element of the solution, retrack using dfs and insert all other elements after it and we get the final solution.just reverse and display it. |[code](https://cses.fi/paste/e1e8733260f2d739675974/) 
[Course Schedule](https://cses.fi/problemset/task/1679)|Simply apply topological sort.Topological sort uses queue|[code](https://cses.fi/paste/98940f58e4b097c9677193/)
[Longest Flight Route](https://cses.fi/problemset/task/1680)|It's an directed acyclic graph so rather than applying dijkstra having complexity O(NlogN) , apply topological sort (O(n)) where it makes sure that a node comes before another node. Then dis[] array can be used efficiently to compute shortest distance as well as maintaning prev connected node.|[code](https://cses.fi/problemset/result/6795375/)
[Game Routes](https://cses.fi/problemset/task/1681)|any directed acyclic graph can be converted to Dynamic programming and any Dynamic programmming problem can be converted to acyclic graph. In this question for possible paths dfs(v)=dfs(u1)+dfs(u2)+...dfs(ui). As dfs closely resembles with  topological sort where one node has to occur previous of another node , here nodes can be arranged in topological order and dp can be applied on each node for its successive node and hence dp[n] can be found out.|[code](https://cses.fi/paste/8bbdd92fdb6b677b679958/)
[Investigation](https://cses.fi/problemset/task/1202)|Simple dijsktra's  problem|[code](https://cses.fi/paste/7dbcb85d61eee28d67c0ef/)
[Planets Queries (Binary Uplifting)](https://cses.fi/problemset/task/1750)|Global variables or arrays are declared in heap memory where as inside function variables stored in  stack.Heap memory can store as large as the constraints on memory are given in online platform.Stack overflow may occur for large size such as 10^7 or 10^8, Hence stack overflow may cause error. therefore declare constant size arrays for large size array globally.cout<<endl also consumes time so use cout<<"\n" .for fast input output use  ios_base::sync_with_stdio(false);   cin.tie(nullptr);   cout.tie(nullptr);|[code](https://cses.fi/paste/6d696e6936a1432467c6c5/) 