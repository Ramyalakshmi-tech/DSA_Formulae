## Let's dry-run next permutation for arr = [4, 2, 5, 3, 1] step by step.

**Step 1: Find the first decreasing element from the right**

Start from the right:

arr[3] = 3 > arr[4] = 1 ❌

arr[2] = 5 > arr[3] = 3 ❌

arr[1] = 2 < arr[2] = 5 ✅ (Found i = 1)

**Step 2: Find the smallest number greater than arr[i]**

Find j such that arr[j] > arr[i]

arr[2] = 5 > arr[1] = 2 ✅ (Found j = 2)

**Check further: arr[3] = 3 > arr[1] = 2 ✅ (Found j = 3, but arr[2] = 5 is larger)**

Choose arr[3] = 3 as it's the smallest valid swap.

**Step 3: Swap arr[i] and arr[j]**

Swap arr[1] and arr[3]

Before Swap: [4, 2, 5, 3, 1]

After Swap: [4, 3, 5, 2, 1]

## Step 4: Reverse the subarray after i

Reverse [5, 2, 1] → [1, 2, 5]

Final array: [4, 3, 1, 2, 5]

✅ Output: [4, 3, 1, 2, 5] (Next permutation)

for string permutations
https://www.geeksforgeeks.org/problems/permutations-of-a-given-string2041/1

import java.util.*;

class Solution {
    public ArrayList<String> findPermutation(String s) {
        char[] arr = s.toCharArray();
        int n = arr.length;

        // Step 1: Find first decreasing character from the end
        int i = n - 2;
        while (i >= 0 && arr[i] >= arr[i + 1]) {
            i--;
        }

        if (i >= 0) {  // Only proceed if a swap is possible
            // Step 2: Find the smallest character larger than arr[i]
            int j = n - 1;
            while (arr[j] <= arr[i]) {
                j--;
            }
            swap(arr, i, j);  // Swap these characters
        }

        // Step 3: Reverse the substring after index `i`
        reverse(arr, i + 1, n - 1);

        // Convert to list for output
        ArrayList<String> result = new ArrayList<>();
        result.add(new String(arr));
        return result;
    }

    private void swap(char[] arr, int i, int j) {
        char temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
    }

    private void reverse(char[] arr, int start, int end) {
        while (start < end) {
            swap(arr, start, end);
            start++;
            end--;
        }
    }
}
