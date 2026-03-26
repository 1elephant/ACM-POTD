#Code -Intermediate
```cpp
class Solution {
public:
    vector<int> productExceptSelf(vector<int>& nums) {
        int l = nums.size();
        vector<int> v;
        int mul = 1;
        for (int i = 0; i < l; i++) {
            if (i == 0) {
                v.push_back(1);
            } else {
                v.push_back(mul);
            }
            mul *= nums[i];
        }
        mul = 1;
        for (int i = l - 1; i > -1; i--) {
            int temp = nums[i];
            if (i == l - 1) {
                nums[i] = v[i];
            } else {
                nums[i] = mul * v[i];
            }
            mul *= temp;
        }
        return nums;
    }
};
```

#Screenshot
<img width="1904" height="788" alt="Screenshot 2026-03-26 090954" src="https://github.com/user-attachments/assets/6e117a6a-0c31-440b-afc5-722dee6ff3c4" />
