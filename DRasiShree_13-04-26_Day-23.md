# Code
```cpp
class Solution {
public:
    int findJudge(int n, vector<vector<int>>& trust) {
        if(n == 1) return 1;
        unordered_map<int,int> utrust;
        unordered_map<int,int> theytrust;
        for(auto i:trust){
            utrust[i[0]]++;
            theytrust[i[1]]++;
        }
        for(auto j:theytrust){
            if(j.second == n-1){
                if(utrust.find(j.first)==utrust.end()){
                    return j.first;
                }
            }
        }
        return -1;    
    }
};
```
# ScreenShot
<img width="1917" height="871" alt="image" src="https://github.com/user-attachments/assets/d3f9670b-3b75-4019-af2c-bc28935782a0" />
