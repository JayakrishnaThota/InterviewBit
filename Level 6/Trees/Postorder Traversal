/**
 * Definition for binary tree
 * class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) {
 *      val = x;
 *      left=null;
 *      right=null;
 *     }
 * }
 */
public class Solution {
    public ArrayList<Integer> postorderTraversal(TreeNode A) {
        ArrayList<Integer> list = new ArrayList();
        if(A==null) return list;
        Stack<TreeNode> stack = new Stack();
        stack.push(A);
        TreeNode prev = null;
        while(!stack.isEmpty()){
            TreeNode cur = stack.peek();
            if(prev==null || prev.left==cur || prev.right==cur){
                if(cur.left!=null){
                    stack.push(cur.left);
                }
                else if(cur.right!=null){
                    stack.push(cur.right);
                }
            }
            else if(cur.left==prev){
                if(cur.right!=null)
                    stack.push(cur.right);
            }
            else{
                list.add(cur.val);
                stack.pop();
            }
            prev = cur;
        }
        return list;
    }
}
