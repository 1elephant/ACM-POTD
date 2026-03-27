# Code-Intermediate
```cpp
class Solution {
public:
    bool checkSubarraySum(vector<int>& nums, int k) {
        unordered_map<int, int> mp;
        mp[0] = -1;   
        int sum = 0;
        for(int i = 0; i < nums.size(); i++) {
            sum += nums[i];
            int rem = sum % k;
            
            if(mp.find(rem) != mp.end()) {
                if(i - mp[rem] >= 2) {
                    return true;
                }
            } else {
                mp[rem] = i;
            }
        }
        return false;
    }
};
```
# ScreenShot
<img width="1919" height="861" alt="image" src="https://github.com/user-attachments/assets/fbe832d9-806f-4d32-bf1d-356f096d2468" />
