# Code
```cpp
class Solution {
public:
    bool isSame(TreeNode* a, TreeNode* b) {
        if (!a && !b) return true;
        if (!a || !b) return false;
        if (a->val != b->val) return false;
        return isSame(a->left, b->left) && isSame(a->right, b->right);
    }

    bool isSubtree(TreeNode* root, TreeNode* subRoot) {
        if (!root) return false;
        if (isSame(root, subRoot)) return true;
        return isSubtree(root->left, subRoot) ||
               isSubtree(root->right, subRoot);
    }
};
```
# ScreenShot
<img width="1919" height="870" alt="image" src="https://github.com/user-attachments/assets/108fb019-ee8e-44c6-8555-d482593f0061" />
