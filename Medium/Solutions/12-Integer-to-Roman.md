#### [Click here to see the question](https://leetcode.com/problems/integer-to-roman/)

## Java

```Java
class Solution {
    public String intToRoman(int num) {
        String[] roman={"I","IV","V","IX","X","XL","L","XC","C","CD","D","CM","M"};
        int[] value={1,4,5,9,10,40,50,90,100,400,500,900,1000};
        int l=value.length-1;
        String st="";
        
        while(num>0){
            if(num/value[l]>0){
                st+=roman[l];
                num-=value[l];
            }
            else{
                l--;
            }
        }
        return st;
    }
}
```
