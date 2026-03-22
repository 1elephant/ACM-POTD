
## Code-Basic:
```cpp
class Solution {
public:
    int removeDuplicates(vector<int>& nums) {
        int n = nums.size();
        int h = 0;
        for(int i = 1; i < n; i++){
            if(nums[i] != nums[h]){
                nums[h+1] = nums[i];
                h++;
            }
        }
        return h + 1;
    }
};
```
## Screenshot:
<img width="1908" height="821" alt="Screenshot 2026-03-22 112020" src="https://github.com/user-attachments/assets/357e1ebf-da29-4326-9795-e4647ba73486" />
