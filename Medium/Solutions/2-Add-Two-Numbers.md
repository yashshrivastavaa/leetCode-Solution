#### [Click here to see the question](https://leetcode.com/problems/add-two-numbers/)

## Java

```Java
class Solution {
    public ListNode addTwoNumbers(ListNode l1, ListNode l2) {
         ListNode l3 = new ListNode();
        ListNode head=l3;
        int carry=0;
        
        while(l1!=null||l2!=null){
            int a=(l1!=null)? l1.val: 0;
            int b=(l2!=null)? l2.val: 0;
            
            int sum=a+b+carry;
            carry=sum/10;
            
            l3.next=new ListNode(sum%10);
            l3=l3.next;
            
            if(l1!=null) l1=l1.next;
            if(l2!=null) l2=l2.next;
        }
        
        if(carry>0){
            l3.next=new ListNode(1);
        }
        
        return head.next;
    }
}
```
