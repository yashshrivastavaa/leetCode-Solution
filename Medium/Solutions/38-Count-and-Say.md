#### [Click here to see the question](https://leetcode.com/problems/count-and-say/)

## Java

```Java
class Solution {
    public String countAndSay(int n) {
        if(n==1) return "1";
        
        String num="1";
        for(int j=2;j<=n;j++){
            String newNum="";
            char current=num.charAt(0);
            int count=0;
            for(int i=0;i<num.length();i++){
                if(current==num.charAt(i))
                    count++;
                else{
                    newNum+=(char)(count+'0');
                    newNum+=current;
                    current=num.charAt(i);
                    count=1;
                }
            }
            newNum+=(char)(count+'0');
            newNum+=current;
            num=newNum;
        }
        return num;
    }
}
```
