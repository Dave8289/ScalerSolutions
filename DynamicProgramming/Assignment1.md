Q1. Stairs

Problem Description
You are climbing a staircase and it takes A steps to reach the top.

Each time you can either climb 1 or 2 steps. In how many distinct ways can you climb to the top?

Return the number of distinct ways modulo 1000000007



Problem Constraints
1 <= A <= 105



Input Format
The first and the only argument contains an integer A, the number of steps.



Output Format
Return an integer, representing the number of ways to reach the top.



Example Input
Input 1:

 A = 2
Input 2:

 A = 3


Example Output
Output 1:

 2
Output 2:

 3


Example Explanation
Explanation 1:

 Distinct ways to reach top: [1, 1], [2].
Explanation 2:

 Distinct ways to reach top: [1 1 1], [1 2], [2 1].


Solution ->

    public int climbStair(int A,int[] dp,int mod) {
        if(A == 0){
            return 1;
        }
        if(A < 0){
            return 0;
        }
        if(dp[A] != 0){
            return dp[A];
        }
        int count = 0;
        for(int i = 1 ; i <= 2 ; i++){
           count = (count%mod + climbStair(A-i,dp,mod)%mod)%mod;
        }
        return dp[A] = count;
    }
    public int climbStairs(int A) {//2->11->2
       return climbStair(A,new int[A+1],1000000007);
    }

    
---------------------------------------------------------------------------------------------------------
Q2. Fibonacci Number TC(O)N SC(O)N

Problem Description
Given a positive integer A, write a program to find the Ath Fibonacci number.

In a Fibonacci series, each term is the sum of the previous two terms and the first two terms of the series are 0 and 1. i.e. f(0) = 0 and f(1) = 1. Hence, f(2) = 1, f(3) = 2, f(4) = 3 and so on.

NOTE: 0th term is 0. 1th term is 1 and so on.



Problem Constraints
0 <= A <= 44



Input Format
First and only argument is an integer A.



Output Format
Return an integer denoting the Ath Fibonacci number.



Example Input
Input 1:

 A = 4
Input 2:

 A = 6


Example Output
Output 1:

 3
Output 2:

 8


Example Explanation
Explanation 1:

 Terms of Fibonacci series are: 0, 1, 1, 2, 3, 5, 8, 13, 21 and so on.
 0th term is 0 So, 4th term of Fibonacci series is 3. 
Explanation 2:

 6th term of Fibonacci series is 8.


Solution ->

    public static int fibDP(int n){
    if(n <= 1 ){
        return n;
    }
     int a = 0;
     int b = 1;
     int fib = 0;
     for(int i = 2 ; i <= n ; i++){
         fib = a + b;
         a = b;
         b = fib;
     }
     return fib;
    }

    
---------------------------------------------------------------------------------------------------------

Q1-> 


Solution ->

    
---------------------------------------------------------------------------------------------------------

Q1-> 


Solution ->

    
---------------------------------------------------------------------------------------------------------

Q1-> 


Solution ->

    
---------------------------------------------------------------------------------------------------------

Q1-> 


Solution ->

    
---------------------------------------------------------------------------------------------------------

Q1-> 


Solution ->

    
---------------------------------------------------------------------------------------------------------

Q1-> 


Solution ->

    
---------------------------------------------------------------------------------------------------------

Q1-> 


Solution ->

    
---------------------------------------------------------------------------------------------------------

