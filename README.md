#User function Template for python3

'''
class Node:
    def _init_(self, val):
        self.right = None
        self.data = val
        self.left = None
'''
# your task is to complete this function

class Solution:
    #Function to convert a binary tree into its mirror tree.
    def mirror(self, root):
        # Code here
        if root is None:
            return None
        mirroredLeft = self.mirror(root.left)
        mirroredRight = self.mirror(root.right)
        root.left = mirroredRight
        root.right = mirroredLeft
        return root
