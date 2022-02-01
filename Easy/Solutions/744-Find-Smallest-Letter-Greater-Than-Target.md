#### [Click Here To See The Question](https://leetcode.com/problems/find-smallest-letter-greater-than-target/)
 
## Java

```Java
class Solution {
    public char nextGreatestLetter(char[] letters, char target) {
        for(char c : letters){
            if(c>target){
                return c;
            }
        }
        return letters[0];
    }
}
```
