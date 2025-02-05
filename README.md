#User function Template for python3



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
