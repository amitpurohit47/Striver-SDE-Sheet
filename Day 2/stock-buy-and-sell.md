```cpp

class Solution {
public:
    int maxProfit(vector<int>& prices) {
        int mi = prices[0], ans = 0;
        for ( auto g : prices ) {
            mi = min(g, mi);
            ans = max(g - mi, ans);
        }
        
        return ans;
        
    }
};

```