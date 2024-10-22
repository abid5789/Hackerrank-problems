

import java.util.Arrays;
class Findtriplet {
    
    static boolean findThreeNumbers(int[] arr, int Sum) {
    
        Arrays.sort(arr);
        int n = arr.length;

        for (int i = 0; i < n - 2; i++) {
            int left = i + 1;  
            int right = n - 1; 

            while (left < right) {
                int currentSum = arr[i] + arr[left] + arr[right];

            
                if (currentSum == Sum) {
                    System.out.println(  arr[i] + ", " + arr[left] + ", " + arr[right]);
                    return true;
                }

            
                if (currentSum < Sum) {
                    left++;
                } else {
                    right--;
                }
            }
        }
        
        
        return false;
    }

    public static void main(String[] args) {
        int[] arr = {12, 3, 4, 1, 6, 9};
        int Sum=24;

        
findThreeNumbers(arr, Sum);
        }
    }
