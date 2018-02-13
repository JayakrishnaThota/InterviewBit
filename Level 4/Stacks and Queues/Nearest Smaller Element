public class Solution {
    public ArrayList<Integer> prevSmaller(ArrayList<Integer> A) {
        ArrayList<Integer> list = new ArrayList();
        Stack<Integer> stack = new Stack();
        for(int i=0;i<A.size();i++){
            int num = A.get(i);
            if(stack.isEmpty()){
                list.add(-1);
            }
            else if(num<=stack.peek()){
                while(!stack.isEmpty() && num<=stack.peek()){
                    stack.pop();
                }
                if(stack.isEmpty()){
                    list.add(-1);
                }
                else
                list.add(stack.peek());
            }
            else
            list.add(stack.peek());
            stack.push(num);
        }
        return list;
    }
}
