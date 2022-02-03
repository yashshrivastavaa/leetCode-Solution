#### [Click here to see the question](https://leetcode.com/problems/container-with-most-water/)

## Java

```Java
class Solution {
    public int maxArea(int[] h) {
        int i=0;
        int j=h.length-1;
        int max=0;
        while(i<j){
            max=Math.max(max,(j-i)*Math.min(h[i],h[j]));
            
            if(h[i]>h[j]){
                j--;
            }
            else if(h[i]<=h[j]){
                i++;
            }
        }  
        return(max);
    }
}
```
