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
