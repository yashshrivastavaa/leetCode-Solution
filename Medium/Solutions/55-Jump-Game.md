#### [Click here to see the question](https://leetcode.com/problems/jump-game/)

## Java

```Java
class Solution {
    
    public boolean canJump(int[] nums) {
        int l=nums.length;
        if(l==1) return true;
        int p=l-1;
        
        for(int i=l-2;i>=0;i--){
            if(i+nums[i]>=p){
                p=i;
            }
        }
        if(p==0)
            return true;
        return false;
    }
}
```
