```cpp

class Solution {
public:
    void rotate(vector<vector<int>>& matrix) {
        
        int n = matrix.size();
        
        for ( int i = 0; i < n; i++ ) {
            for ( int j = n - 1; j >= n - i; j-- ) {
                swap(matrix[i][j], matrix[n - j - 1][n - i - 1]);
            }
        }
        
        int i = 0, j = n - 1;
        
        while ( i < j ) {
            swap(matrix[i], matrix[j]);
            i++;
            j--;
        }
        
    }
};

```