# Code - Intermediate

``` cpp
class Solution {
public:
    ListNode* deleteDuplicates(ListNode* head) {
        ListNode dummy(0, head);
        ListNode* pp = &dummy;
        ListNode* pre = head;
        ListNode* temp = head;
        while(temp != NULL){
            bool dup = false;
            while(temp->next != NULL && temp->val == temp->next->val){
                dup = true;
                temp = temp->next;
            }
            if(dup){
                pp->next = temp->next;
            }
            else{
                pp = pre;
            }
            temp = temp->next;
            pre = temp;
        }
        return dummy.next;
    }
};
```
# ScreenShot
<img width="1912" height="791" alt="image" src="https://github.com/user-attachments/assets/ddf46555-0e1f-4856-8e88-0d51715473e6" />
