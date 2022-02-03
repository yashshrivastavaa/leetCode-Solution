#### [Click here to see the question](https://leetcode.com/problems/set-matrix-zeroes/)

## Java

```Java
import java.util.Arrays;
class Solution {
    public void setZeroes(int[][] mat) {
        boolean col = false;
        int m=mat.length;
        int n=mat[0].length;
        
        for(int i=0;i<m;i++){
            for(int j=0;j<n;j++){
                if(mat[i][j]==0)
                    if(j>0) {
                        mat[0][j]=0;
                        mat[i][0]=0;
                    }
                    else col=true;       
            }
        }
        
        for(int i=m-1;i>=0;i--){
            for(int j=n-1;j>=1;j--){
                if(mat[0][j]==0||mat[i][0]==0)
                    mat[i][j]=0;
            }
        }
        
        for(int j=0;j<m;j++){
            if(col)
                mat[j][0]=0;
        }
        
        System.out.print(Arrays.deepToString(mat));
        
    }
}
```
