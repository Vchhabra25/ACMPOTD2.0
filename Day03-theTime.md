Problem : 
Find and print the time after a minutes.

Approach : 
The main thing is minutes ka carry into hours and then 24-hour clock ka wrap-around.

CODE : java

import java.util.*;

public class theTime {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        String time=sc.next();
        int a=sc.nextInt();

        int hr=Integer.parseInt(time.substring(0,2));
        int min=Integer.parseInt(time.substring(3,5));

        int total=hr*60+min+a;
        hr=(total/60)%24;
        min=total%60;


        System.out.printf("%02d:%02d%n",hr,min);
    }
}

TC=O(1)
SC=O(1)
<img width="920" height="344" alt="Screenshot 2026-10-05 at 3 21 16 PM" src="https://github.com/user-attachments/assets/ca6024ba-9efb-4852-99f9-96ea2f38f714" />
