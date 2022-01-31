#### [Click Here To See The Question](https://leetcode.com/problems/reshape-the-matrix/)

## Java

```Java
class Solution {
    public int[][] matrixReshape(int[][] mat, int r, int c) {
        int[][] arr = new int[r][c];
        if(mat.length * mat[0].length != r*c)
            return mat;
        int row = 0;
        int col = 0;
        for(int i = 0;i<mat.length;i++) {
            for(int j = 0;j<mat[0].length;j++) {
                arr[row][col]=mat[i][j];
                col++;
                if(col==c){
                    col=0;
                    row++;
                }
            }
        }
        return arr;
    }
}
```
