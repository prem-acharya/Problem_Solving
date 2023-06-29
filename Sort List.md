Question -> Sort List


Given the head of a linked list, return the list after sorting it in ascending order.

Example 1:

![Alt text](https://assets.leetcode.com/uploads/2020/09/14/sort_list_1.jpg)
```
Input: head = [4,2,1,3]
Output: [1,2,3,4]
```

Example 2:

![Alt text](https://assets.leetcode.com/uploads/2020/09/14/sort_list_2.jpg)
```
Input: head = [-1,5,3,4,0]
Output: [-1,0,3,4,5]
```

Example 3:

```
Input: head = []
Output: []
``` 

Constraints:

- The number of nodes in the list is in the range [0, 5 * 104].
- -105 <= Node.val <= 105

C++ Code:
```C++
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode() : val(0), next(nullptr) {}
 *     ListNode(int x) : val(x), next(nullptr) {}
 *     ListNode(int x, ListNode *next) : val(x), next(next) {}
 * };
 */
class Solution {
public:
    ListNode* sortList(ListNode* head) {

        if(head==NULL)
        {
            return NULL;
        }
        vector<int> k;
        ListNode* ptr = head;

        while(ptr!=NULL)
        {
            k.push_back(ptr->val);
            ptr=ptr->next;
        }

        sort(k.begin(),k.end());

        ptr=head;
        int i=0;

        while(ptr!=NULL)
        {
            ptr->val=k[i++];
            ptr=ptr->next;
        }

        return head;
    }
};
```
