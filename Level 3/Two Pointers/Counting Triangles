public class Solution {
    public int nTriang(ArrayList<Integer> A) {
        int[] nums = new int[A.size()];
        for(int i=0;i<nums.length;i++)
        nums[i] = A.get(i);
        long count = 0;
        Arrays.sort(nums);
        for (int i = 0; i < nums.length - 2; i++) {
            int k = i + 2;
            for (int j = i + 1; j < nums.length - 1 && nums[i] != 0; j++) {
                while (k < nums.length && nums[i] + nums[j] > nums[k])
                    k++;
                count += k - j - 1;
                count%=1000000007;
            }
        }
        return (int)(count%1000000007);
    }
}
