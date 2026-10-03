Problem : 
Take everything because all numbers are positive. If the total is odd, remove the smallest odd number to make the sum even.

Approach : 
We want the maximum sum that is even.
- Take all even numbers — they never cause a parity problem.
- Take all odd numbers too.
- If the number of odd elements is even, total sum is already even → answer is total sum.
- If the number of odd elements is odd, total sum is odd. To lose as little as possible, remove the smallest odd number.

CODE : java

import java.util.*;

public class wetShark {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();

        long sum=0;
        int minOddElement=Integer.MAX_VALUE;

        for(int i=0;i<n;i++){
            int x=sc.nextInt();

            sum+=x;
            if(x%2!=0){
                minOddElement=Math.min(minOddElement,x);
            }
        }
        if(sum%2!=0){
            sum-=minOddElement;
        }
        System.out.println(sum);
    }
}
<img width="792" height="382" alt="Screenshot 2026-10-04 at 2 24 35 AM" src="https://github.com/user-attachments/assets/a0033b6a-e053-44f5-aea8-a33e5386aad5" />

TC=O(n)
SC=O(1)
