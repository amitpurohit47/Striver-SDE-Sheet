```cpp

class Solution {
public:
    vector<vector<int>> generate(int n) {
        vector<vector<int>> ans;
        ans.push_back({ 1 });
        
        if ( n == 1 ) return ans;
        
        ans.push_back({ 1, 1 });
        
        if ( n == 2 ) return ans;
        
        n -= 2;
        
        while ( n-- ) {
            vector<int> v = ans.back(), v1;
            v1.push_back(1);
            
            for ( int i = 0; i < v.size() - 1; i++ ) v1.push_back(v[i] + v[i + 1]);
            v1.push_back(1);
            
            ans.push_back(v1);
        }
        
        return ans;
        
    }
};

```