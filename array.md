```java
class Solution {
    public int findMaxConsecutiveOnes(int[] nums) {
        int res = 0;
        for (int i = 0; i < nums.length; i++) {
            int j = i;
            while (j < nums.length && nums[j] == 1) j++;
            res = Math.max(res, j - i);
            i = j;
        }
        return res;
    }
}
```

