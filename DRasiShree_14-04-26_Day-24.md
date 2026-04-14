# Code
```cpp
class Solution {
public:
    int findCenter(vector<vector<int>>& edges) {
        if(edges[0][0] == edges[1][0] || edges[0][0] == edges[1][1])
            return edges[0][0];
        return edges[0][1];
    }
};
```
# ScreenShoot
<img width="1919" height="863" alt="image" src="https://github.com/user-attachments/assets/5bca3213-30dc-4e88-b609-ec90201a3fee" />
