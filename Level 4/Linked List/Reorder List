/**
 * Definition for singly-linked list.
 * class ListNode {
 *     public int val;
 *     public ListNode next;
 *     ListNode(int x) { val = x; next = null; }
 * }
 */
public class Solution {
    ListNode getMiddleNode(ListNode a){
        ListNode one = a, two = a.next;
        if(two != null)
            two = two.next;
        while(two != null){
            two = two.next;
            if(two != null)
                two = two.next;
            
            one = one.next;
        } 
        return one;
    }
    
    ListNode reverse(ListNode a){
        if(a == null || a.next == null)
            return a;
        ListNode current = null, prev = null;
        while(a != null){
            current = a;
            a = a.next;
            current.next = prev;
            prev = current;
        }
        
        return current;
    }
	public ListNode reorderList(ListNode a) {
	    if(a == null || a.next == null)
	        return a;
	    
	    ListNode m = getMiddleNode(a);
	    ListNode second = m.next;
	    m.next = null;
	    ListNode first = a;
	    second = reverse(second);
	    
	    ListNode head, end;
	    head = end = first;
	    first = first.next;
	    boolean addFirst = false;
	    while(first != null && second != null){
	        if(addFirst){
	            end.next = first;
	            end = first;
	            first = first.next;
	        }
	        else{
	            end.next = second;
	            end = second;
	            second = second.next;
	        }
	        addFirst = !addFirst;
	    }
	    if(first != null)
	        end.next = first;
	    else
	        end.next = second;
	    
	    return head;     
	    
	}
}
