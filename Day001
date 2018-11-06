import java.util.Arrays;
import java.util.HashMap;
import java.util.Map;

/**
 * Two Sum
 * Given an array of integers, return indices of the two numbers such that they add up to a specific target.
 *
 * You may assume that each input would have exactly one solution, and you may not use the same element twice
 *
 * Example:
 *
 * Given nums = [2, 7, 11, 15], target = 9,
 *
 * Because nums[0] + nums[1] = 2 + 7 = 9,
 * return [0, 1].
 * @author foxcles
 * @date   2018/11/6 8:36
 * @since  1.0
 */
public class SumNumber {
    public static int[] twoSum(int[] nums, int target) {
        return method2(nums, target);

    }

    private static int[] method1(int[] nums, int target) {

        int[] result = new int[2];
        if (nums.length > 0) {
            int[] nums2 = nums;
            loop:
            for (int i = 0; i < nums.length; i++) {
                for (int j = 0; j < nums2.length; j++) {
                    while (nums[i] + nums2[j] == target) {
                        result[0] = i;
                        result[1] = j;
                        break loop;
                    }
                }
            }
        }
        return result;
    }

    private static int[] method2(int[] nums, int target) {

        Map<Integer, Integer> res = new HashMap<>(16);
        int[] result = new int[2];
        if (nums.length > 0) {
            for (int n = 0; n < nums.length; n++) {
               res.put(nums[n], n);
            }
            for (int i = 0; i < nums.length; i++) {
                int t = target-nums[i];
                if (res.containsKey(t) && res.get(t) != i) {
                    result[0] = i;
                    result[1] = res.get(t);
                }
            }
        }
        return result;
    }


    public static void main(String[] args) {
        int[] nums = {3, 2, 4};
        int target = 6;
        int[] res = twoSum(nums, target);
        System.out.println(Arrays.toString(res));

    }


}
