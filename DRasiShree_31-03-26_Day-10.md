# Code - Intermediate
``` cpp
class Solution {
public:
    ListNode* addTwoNumbers(ListNode* l1, ListNode* l2) {
        ListNode* dummy = new ListNode(0);
        ListNode* curr = dummy;
        int carry = 0;
        while (l1 != NULL || l2 != NULL || carry) {
            int sum = carry;
            if (l1) {
                sum += l1->val;
                l1 = l1->next;
            }
            if (l2) {
                sum += l2->val;
                l2 = l2->next;
            }
            carry = sum / 10;
            curr->next = new ListNode(sum % 10);
            curr = curr->next;
        }
        return dummy->next;
    }
};
```

# ScreenShot
<img width="1904" height="800" alt="Screenshot 2026-03-31 080908" src="https://github.com/user-attachments/assets/7538674d-6b1a-4b74-ae2f-713cc5f96de4" />
