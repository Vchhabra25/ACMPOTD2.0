Problem : 
In this problem you are to calculate the sum of all integers from 1 to n, but you should take all powers of two with minus in the sum.
 
Initial Thought Process
Initially, I misunderstood the problem as if we were given multiple integers and had to check whether each integer itself was a power of 2.
I thought:
- If the number is a power of 2 → subtract it.
- Otherwise → add it.

Final Approach:
-Calculate the normal sum from 1 to n.
-Generate all powers of 2 up to n.
-For each power of 2, subtract 2 × power from the sum.
-Print the answer.

CODE : java
<img width="882" height="286" alt="Screenshot 2026-10-01 at 8 42 01 PM" src="https://github.com/user-attachments/assets/fc3fd690-9ffb-4318-9a03-db104958a094" />

import java.util.*;

public class trickySum {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);

        int t=sc.nextInt();
        while(t-->0){
            long n=sc.nextLong();
            long ans=n*(n+1)/2;

            for(long p=1;p<=n;p*=2){
                ans=ans-2*p;
            }
            System.out.println(ans);
        }
    }
}


TC=O(log n)
SC=O(1)

