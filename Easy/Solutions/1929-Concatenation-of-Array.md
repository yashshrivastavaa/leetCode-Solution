#### [Click here to see the question](https://leetcode.com/problems/concatenation-of-array/)

## Java
```Java
class Solution {
    public int[] getConcatenation(int[] nums) {
        int n = nums.length;
        int[] arr = new int[n*2];
        for(int i = 0;i<n;i++){
            arr[i]=nums[i];
            arr[i+n]=nums[i];
        }
        return arr;
    }
}
```

## Python
```Python
class Solution:
  def getConcatenation(self, nums: List[int]) -> List[int]:
    return nums * 2
```

## C==
``cpp
class Solution {
 public:
  vector<int> getConcatenation(vector<int>& nums) {
    const int n = nums.size();

    for (int i = 0; i < n; ++i)
      nums.push_back(nums[i]);

    return nums;
  }
};
```
