```cpp
class Solution {
public:
    void nextPermutation(vector<int>& nums) {
        
        if ( nums.size() == 1 ) return;
        
        int k = nums.size() - 2;
        
        while ( k >= 0 && nums[k] >= nums[k + 1] ) k--;
        
        if ( k < 0 ) {
            reverse(nums.begin() + k + 1, nums.end());
            return;
        }
        
        for ( int i = nums.size() - 1; i > k; i-- ) {
            if ( nums[i] > nums[k] ) {
                swap(nums[k], nums[i]);
                break;
            }
        }
        
        reverse(nums.begin() + k + 1, nums.end());
    }
};
```