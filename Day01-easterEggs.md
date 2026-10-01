Problem : 
The Easter Rabbit laid n eggs in a circle and is about to paint them.
-Each egg should be painted one color out of 7: red, orange, yellow, green, blue, indigo or violet. Also, the following conditions should be satisfied:
--Each of the seven colors should be used to paint at least one egg.
--Any four eggs lying sequentially should be painted different colors.
--Help the Easter Rabbit paint the eggs in the required manner. We know that it is always possible.

Approach: 
Use ROYGBIV once to include all 7 colors, then repeat GBIV for the remaining eggs so that every 4 consecutive eggs have different colors, 
including around the circle.

CODE : java

import java.util.*;

public class easterEggs {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();

        String ans="ROYGBIV";
        String patternToRepeat="GBIV";

        for(int i=0;i<n-7;i++){
            ans+=patternToRepeat.charAt(i%4);
        }

        System.out.println(ans);
    }
}

<img width="729" height="279" alt="Screenshot 2026-10-02 at 1 12 54 AM" src="https://github.com/user-attachments/assets/1139f74c-4d7b-4bd4-91fd-fb342e5d52e0" />

TC=O(n)
SC=O(n)
