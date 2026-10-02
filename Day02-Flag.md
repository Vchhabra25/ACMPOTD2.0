Problem : 
Given an n × m grid representing a flag, check whether:
- Every row contains only one color (all m elements in a row are the same).
- Adjacent rows have different colors.
Print YES if both conditions hold, otherwise NO.

Thought process : 
For each row, check that all its elements are the same as the first element.
Then check that the color of every row differs from the previous row; if both conditions hold, print YES.

CODE : java
import java.util.*;
public class flag {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int m=sc.nextInt();

        char[][] arr=new char[n][m];

        for(int i=0;i<n;i++){
            arr[i]=sc.next().toCharArray();
        }

        for(int i=0;i<n;i++){
            for(int j=1;j<m;j++){
                if(arr[i][j]!=arr[i][0]){
                    System.out.println("NO");
                    return;
                }
            }

            if(i>0 && arr[i][0]==arr[i-1][0]){
                System.out.println("NO");
                return;
            }
        }
        System.out.println("YES");
    }
}


TC=O(nxm)
SC=O(nxm)

<img width="822" height="455" alt="Screenshot 2026-10-03 at 4 00 32 AM" src="https://github.com/user-attachments/assets/7e007412-14d0-4ea0-9e08-9b7efa56354e" />
