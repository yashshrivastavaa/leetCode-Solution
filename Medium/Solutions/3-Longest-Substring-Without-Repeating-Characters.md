#### [Click here to see the question](https://leetcode.com/problems/longest-substring-without-repeating-characters/)

## Java

```Java
import java.util.*;
class Solution {
    public int lengthOfLongestSubstring(String s) {
       int len=s.length();
        
        int max=0,start=0;
        HashMap<Character,Integer> map= new HashMap<>(); 
        for(int end=0;end<len;end++){
            char ch=s.charAt(end);
            
            if(map.containsKey(ch)){
                start=Math.max(map.get(ch),start);
            }
            
            max=Math.max(max,end-start+1);
            
            map.put(ch,end+1);
        }
        
        return max;
        
    }
}
```
