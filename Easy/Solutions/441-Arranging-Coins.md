#### [Click here to see the question]()

## Java - O(n)

```Java
class Solution {
    public int arrangeCoins(int n) {
        long start = 0;
        long end = n;
        while(start <= end) {
            long mid = start + ( end - start) / 2;
            if(mid*(mid+1)/2 == n) {
                return (int)mid;
            }
            else if(mid*(mid+1)/2 < n) {
                start = mid + 1;
            }else{
                end = mid - 1;
            }
        }
        return (int)end;
    }
}
```

## Java - O(1)

```Java
class Solution {
    public int arrangeCoins(int n) {
        return (int) (-0.5 + Math.sqrt(2 * (long)n + 0.25));
    }
}
```
