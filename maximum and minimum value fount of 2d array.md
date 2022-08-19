import java.util.*;
public class SumOfSubArrays {
    public static void main(String args[])
    {
       Scanner sc=new Scanner(System.in);
       int mat[][]=new int[3][3];
       int n=mat.length,m=mat[0].length;
       //input
       for(int i=0;i<n;i++)
       {
        for(int j=0;j<m;j++)
        {
            mat[i][j]=sc.nextInt();
        }
       }
       //output
       for(int i=0;i<n;i++)
       {
        for(int j=0;j<m;j++)
        {
            System.out.print(mat[i][j]+" ");
        }
        System.out.println();
       }
       search(mat);
   }
   public static void search(int mat[][])
   {
    int max=Integer.MIN_VALUE;
    int min=Integer.MAX_VALUE;
    for(int i=0;i<mat.length;i++)
       {
        for(int j=0;j<mat[0].length;j++)
        {
           if(mat[i][j]>max)
           {
            max=(mat[i][j]);
           }
           if(mat[i][j]<min)
           {
              min=(mat[i][j]);
           }
        }
       }
       System.out.println("max value is :"+max);
       System.out.println("min value is :"+min);
   }
}
