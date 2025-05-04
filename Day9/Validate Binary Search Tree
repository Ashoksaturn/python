# Definition for a binary tree node.
# class TreeNode(object):
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution(object):
    def isValidBST(self, root):
        
        def traversal(root,left,right):

            if root ==None:

                return True

            if not(left<root.val<right):

                return False

            return traversal(root.left,left,root.val) and traversal(root.right,root.val,right)
        return traversal(root,float("-inf"),float("inf"))



            
        
