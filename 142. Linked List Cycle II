Time: O(n)
Space: O(1)

https://leetcode.com/problems/linked-list-cycle-ii/description/

public class Solution {
    public ListNode detectCycle(ListNode head) {
        ListNode tortoise = head;
        ListNode hare = head;

        while(hare != null && hare.next != null){
            tortoise = tortoise.next;
            hare = hare.next.next;

            if(tortoise == hare){
                break;
            }
        }

        if(hare == null || hare.next == null){
            return null;
        }

        hare = head;


        while(tortoise != hare){
            tortoise = tortoise.next;
            hare = hare.next;
        }

        return hare;
    }
}
