#### [Click here to see the question](https://leetcode.com/problems/first-bad-version/)

## Java

```Java
public class Solution extends VersionControl {
    public int firstBadVersion(int n) {
        int start = 0, end = n;
        int ans = 0;
        while(start <= end) {
            int mid = start + ( end - start) / 2;
            if(isBadVersion(mid) == true) {
                ans = mid;
                end = mid - 1;
            }else{
                start = mid +1;
            }
        }
        return ans;
    }
}
```
