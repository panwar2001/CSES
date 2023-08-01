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
