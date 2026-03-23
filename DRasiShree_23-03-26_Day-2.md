#code-Intermediate:
class Solution {
public:
    int subarraySum(vector<int>& nums, int k) {
        int count=0;
        for(int i=0;i<nums.size();i++){
            int sum=0;
            for(int j=i;j<nums.size();j++){
                sum+=nums[j];
                if(sum==k){
                    count++;
                }    
            }
        }
        return count;
    }
};

# ScreenShot
<img width="1915" height="753" alt="Screenshot 2026-03-23 122235" src="https://github.com/user-attachments/assets/72e1ef1c-6a81-4f9c-9a99-32a04457e466" />
