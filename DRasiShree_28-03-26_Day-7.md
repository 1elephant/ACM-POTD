# Code - Intermediate
```cpp
class Solution {
public:
    bool increasingTriplet(vector<int>& nums) {
        int first = INT_MAX, second = INT_MAX;
        for (int num : nums) {
            if (num <= first) {
                first = num;
            } else if (num <= second) {
                second = num;
            } else {
                return true;
            }
        }
        return false;
    }
};
```
# ScreenShot
<img width="1916" height="888" alt="Screenshot 2026-03-28 230019" src="https://github.com/user-attachments/assets/73d39d70-5b16-461e-95bf-a243c5a1e932" />
