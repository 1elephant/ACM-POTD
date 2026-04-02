# Code -Intermediate
```cpp
class Solution {
public:
    ListNode* rotateRight(ListNode* head, int k) {
        if (!head || !head->next || k == 0) return head;
        int c = 0;
        ListNode* temp = head;
        while (temp != NULL) {
            c++;
            temp = temp->next;
        }
        k = k % c;
        if (k == 0) return head;
        temp = head;
        for (int i = 0; i < c - k - 1; i++) {
            temp = temp->next;
        }
        ListNode* newHead = temp->next;
        temp->next = NULL;
        ListNode* tail = newHead;
        while (tail->next != NULL) {
            tail = tail->next;
        }
        tail->next = head;
        return newHead;
    }
};
```
# ScreenShot
<img width="1919" height="853" alt="image" src="https://github.com/user-attachments/assets/7507f13a-d9a7-4f85-8c1c-be9f72802e95" />
