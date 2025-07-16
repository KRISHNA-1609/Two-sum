# Two-sum
import java.util.*;

public class Solution {
    public static int[] twoSum(int[] nums, int target) {
        for (int i = 0; i < nums.length; i++) {
            for (int j = i + 1; j < nums.length; j++) {
                if (nums[i] + nums[j] == target) {
                    return new int[]{i, j};
                }
            }
        }
        return new int[]{-1, -1}; // Not found
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        // Example: Input format: 4 2 7 11 15 (first number is size)
        System.out.println("Enter size of array:");
        int n = sc.nextInt();
        int[] nums = new int[n];
        
        System.out.println("Enter array elements:");
        for (int i = 0; i < n; i++) {
            nums[i] = sc.nextInt();
        }

        System.out.println("Enter target:");
        int target = sc.nextInt();

        int[] result = twoSum(nums, target);
        if (result[0] != -1) {
            System.out.println("[" + result[0] + ", " + result[1] + "]");
        } else {
            System.out.println("No valid pair found.");
        }
    }
}
