Problem : 
Given a grid containing '.' and '*', find the smallest rectangle
that contains all the shaded cells ('*').

Thought process : 
When i looked at the question and the example test cases, i understood that it is the boundary of '*' that is returned. 
So find the boundary and give that as entire result.

CODE : java

import java.util.*;
public class letter {
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);

        int n=sc.nextInt();
        int m=sc.nextInt();
        char[][] a=new char[n][m];

        int minRow=n;
        int maxRow=0;
        int minCol=m;
        int maxCol=0;

        for(int i=0;i<n;i++){
            a[i]=sc.next().toCharArray();

            for(int j=0;j<m;j++){
                if(a[i][j]=='*'){
                    minRow=Math.min(minRow,i);
                    maxRow=Math.max(maxRow,i);
                    minCol=Math.min(minCol,j);
                    maxCol=Math.max(maxCol,j);
                }
            }
        }

        for(int i=minRow;i<=maxRow;i++){
            for(int j=minCol;j<=maxCol;j++){
                System.out.print(a[i][j]);
            }
            System.out.println();
        }
    }
}

TC=O(nxm)
SC=O(nxm)

<img width="722" height="580" alt="Screenshot 2026-10-01 at 3 56 30 PM" src="https://github.com/user-attachments/assets/3998eda3-42d7-4e09-ab66-ca0c0603650f" />
