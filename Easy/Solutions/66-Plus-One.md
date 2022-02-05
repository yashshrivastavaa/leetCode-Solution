#### [Click here to see the question](https://leetcode.com/problems/plus-one/)

## Java

```Java
class Solution {
    public int[] plusOne(int[] d) {
        for(int i = d.length-1;i>=0;i--) {
            if(d[i]<9) {
                d[i]++;
                return d;
            }
            d[i]=0;
        }
        d = new int[d.length + 1];
        d[0]=1;
        return d;
    }
}
```
