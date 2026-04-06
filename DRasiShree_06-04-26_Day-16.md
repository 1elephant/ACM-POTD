# Code- Intermediate
```cpp
class Solution {
public:
    vector<int> dailyTemperatures(vector<int>& temperatures) {
        int l = temperatures.size();
        vector<int> v(l, 0); 
        stack<int> s;       

        for (int i = 0; i < l; i++) {
            while (!s.empty() && temperatures[s.top()] < temperatures[i]) {
                int idx = s.top();
                s.pop();
                v[idx] = i - idx;
            }
            s.push(i);
        }
        return v;
    }
};
```
# ScreenShot
<img width="1917" height="811" alt="image" src="https://github.com/user-attachments/assets/bcfd3398-40b1-46c9-a3d8-e0dce8dd7979" />
