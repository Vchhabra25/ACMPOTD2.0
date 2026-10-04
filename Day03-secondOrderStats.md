Problem : 
find second smallest distinct element.

Approach : 
Second smallest but strictly so distinct and hence use hashSet.

CODE : java

import java.util.*;

public class secondOrderStats {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        HashSet<Integer> set=new HashSet<>();

        for(int i=0;i<n;i++){
            set.add(sc.nextInt());
        }

        if(set.size()<2){
            System.out.println("NO");
            return;
        }

        int min=Integer.MAX_VALUE;
        for(int x:set){
            min=Math.min(min,x);
        }
        int second=Integer.MAX_VALUE;
        for(int x:set){
            if(x>min){
                second=Math.min(second,x);
            }
        }
        System.out.println(second);
    }
}

TC=O(n)
SC=O(n)
<img width="574" height="478" alt="Screenshot 2026-10-05 at 12 18 14 AM" src="https://github.com/user-attachments/assets/ebd1292c-e747-46e4-a045-0f9c422972f3" />
