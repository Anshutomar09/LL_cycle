# LL_cycle


/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution {
public:
    bool hasCycle(ListNode *head) {
         ListNode*slow=head;
        ListNode*fast=head;
        if(head==NULL)
            return false;
        
        while(fast and fast->next){//by middle approch
            slow=slow->next;
            fast=fast->next->next;
             if(slow==fast)
                 return true;
             
           
        }
        return false;
    }
};
