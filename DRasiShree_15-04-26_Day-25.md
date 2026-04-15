# Code
```cpp
class Solution {
public:
    int maxDepth(TreeNode* root) {
        if(root == NULL) return 0;

        int left = maxDepth(root->left);
        int right = maxDepth(root->right);

        return 1 + max(left, right);
    }
};
```
# ScreenShot
<img width="1919" height="875" alt="image" src="https://github.com/user-attachments/assets/ba7bbc33-557b-47fb-8adf-2699619513e4" />
