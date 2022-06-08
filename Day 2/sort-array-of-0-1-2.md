```cpp

class Solution {
public:
    void sortColors(vector<int>& nums) {
        int i = -1, j = nums.size();
        for ( int k = 0; k < j; k++ ) {
            if ( nums[k] == 0 ) {
                swap(nums[i + 1], nums[k]);
                i++;
            } else if ( nums[k] == 2 ) {
                swap(nums[j - 1], nums[k]);
                j--;
                k--;
            }
        }
    }
};

```