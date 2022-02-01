#### [Click here to see the question](https://leetcode.com/problems/sqrtx/)

## Java

```Java
class Solution {
    public int mySqrt(int x) {
        // return (int)Math.sqrt(x); // Here we are not allowed to use this!!
        long start = 0;
        long end = x;
        
        while (start + 1 < end) {
            long mid = start + (end - start) / 2;
            if (mid * mid == x) {
                return (int)mid;
            } else if (mid * mid < x) {
                start = mid;
            } else {
                end = mid;
            }
        }
        if (end * end == x) {
            return (int)end;
        }
        return (int)start;
    }
}
```
