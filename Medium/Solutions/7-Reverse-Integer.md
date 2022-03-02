#### [Click here to see the question](https://leetcode.com/problems/reverse-integer/)

## Java

```Java
class Solution {
    public int reverse(int x) {
        boolean isNeg=false;
        
        if(x<0){
            isNeg=true;
            x=Math.abs(x);
        }
        int rev=0;
        while(x>0){
            if (rev > Integer.MAX_VALUE/10 || (rev == Integer.MAX_VALUE / 10 && x%10 > 7)) return 0;
            if (rev < Integer.MIN_VALUE/10 || (rev == Integer.MIN_VALUE / 10 && x%10 < -8)) return 0;
            rev= rev*10 + x%10;
            x/=10;
        }

        if(isNeg){
            rev=-rev;
        }
        
        return rev;
    }
}
```
