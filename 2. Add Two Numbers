Task: https://leetcode.com/problems/add-two-numbers/

Time: O(max(M,N))
Space: O(max(M,N))

class Solution {
    public ListNode addTwoNumbers(ListNode l1, ListNode l2) {
        if(l1 == null){
            return l2;
        } else if (l2 == null){
            return l1;
        }

        int rest = 0;
        ListNode head = null;
        ListNode iter = null;
        while(l1 != null || l2 != null){
            int first = l1 == null ? 0 : l1.val;
            int second = l2 == null ? 0 : l2.val;
            int sum = first + second + rest;
            int digit = sum % 10;
            rest = sum / 10;
            if(head == null){
                head = new ListNode(digit);
                iter = head;
            } else {
                iter.next = new ListNode(digit);
                iter = iter.next; 
            }

            if(l1 != null){
                l1 = l1.next;
            }

            if(l2 != null){
                l2 = l2.next;
            }
        }

        if(rest > 0){
            iter.next = new ListNode(rest);
        }

        return head;
    }
}
