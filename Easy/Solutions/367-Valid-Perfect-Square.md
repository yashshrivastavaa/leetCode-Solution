#### [367. Valid Perfect Square](https://leetcode.com/problems/valid-perfect-square/)

## Java

```Java
class Solution {
    public boolean isPerfectSquare(int num) {
        long start = 1,end = num;
        if(num == 1) {
            return true;
        }
        while(start <= end){
            long mid = start + ( end - start)/2;
            if(mid*mid == num){
                return true;
            }else if(mid*mid < num){
                start = mid +1;
            }else{
                end = mid - 1;
            }
        }
        return false;
    }
}
```
