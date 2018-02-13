public class Solution {
    public ArrayList<ArrayList<Integer>> permute(ArrayList<Integer> A) {
        int[] nums = new int[A.size()];
        for(int i=0;i<nums.length;i++)
        nums[i] = A.get(i);
        ArrayList<ArrayList<Integer>> list = new ArrayList();
        helper(list, new ArrayList<>(), nums);
        return list;
    }
    public void helper(ArrayList<ArrayList<Integer>> list, ArrayList<Integer> sublist, int[] nums){
        if(sublist.size()==nums.length){
            list.add(new ArrayList(sublist));
            return;
        }
        for(int i=0;i<nums.length;i++){
            if(sublist.contains(nums[i])) continue;
            sublist.add(nums[i]);
            helper(list, sublist, nums);
            sublist.remove(sublist.size()-1);
        }
    }
}
