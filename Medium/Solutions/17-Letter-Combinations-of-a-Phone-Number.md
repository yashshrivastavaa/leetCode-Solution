#### [Click here to see the question](https://leetcode.com/problems/letter-combinations-of-a-phone-number/)

## Java

```Java
class Solution {
    
    public List<String> letterCombinations(String d) {
        int l=d.length();
        String[] data={" "," ","abc","def","ghi","jkl","mno","pqrs","tuv","wxyz"};
        
        List<String> ans=new ArrayList<>();
        
        for(int i=0;i<l;i++){
            int index=(int) (d.charAt(i)-'0');
            ans=iterate(ans,toList(data[index]));
        }
        return ans;
    }
    
    public static List<String> iterate(List<String> a, List<String> b){
        int alen=a.size();
        int blen=b.size();
        
        if(alen==0) return b;
        
            List<String> ans=new ArrayList<>();
            for(int i=0;i<alen;i++){
                for(int j=0;j<blen;j++){
                    ans.add(a.get(i).concat(b.get(j)));                
                }
            }
        return ans;
    }
    
    public static List<String> toList(String st){
        int l=st.length();
        List<String> list=new ArrayList<>();
        for(int i=0;i<l;i++){
            list.add(String.valueOf(st.charAt(i)));
        }
        return list;
    }
}
```
