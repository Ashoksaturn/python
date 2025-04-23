class Solution(object):
    def removeNthFromEnd(self, head, n):
        if head is None:
            return head
        
        ptr = head
        count = 0
        while ptr is not None:
            count += 1
            ptr = ptr.next
        
        if count == n:
            head = head.next
            return head
        
        ptr = head
        n = count - n - 1
        count = 0
        while ptr is not None:
            if count == n:
                ptr.next = ptr.next.next
            count += 1
            ptr = ptr.next
        
        return head
