# bt_leetcode_b1
Ransom Note

    class Solution {
      bool canConstruct(String ransomNote, String magazine) {
        if(ransomNote.length > magazine.length) {
            return false;
        }
        List<String> str1 = magazine.split('');
        List<String> str2 = ransomNote.split('');

        for(int i = 0; i < str1.length; i++) {
          for(int j = 0; j < str2.length; j++) {
            if(str2[j] == str1[i]) {
              str2.removeAt(j);
              str1[i] = '';
            }
            if(str2.isEmpty) {
                return true;
            }
          }
        }
        return str2.isEmpty;
      }
    }

Fizz Buzz

    class Solution {
      List<String> fizzBuzz(int n) {
          List<String> answer =[];

          for(int i = 1; i <= n ;i++){
              bool isDivisibleBy3 = i % 3 ==0;
              bool isDivisibleBy5 = i % 5 ==0;

              String currentString = "";
              if(isDivisibleBy3) {currentString += "Fizz";}
              if(isDivisibleBy5) {currentString +="Buzz";}
              if(currentString.isEmpty){
                  currentString +="$i";
              }
              answer.add(currentString);
          }
          return answer;
      }
    }

Defanging an IP Address

    public class Solution {
        public string DefangIPaddr(string address) {
            return address.Replace(".", "[.]");
        }
    }
    
Final Value of Variable After Performing Operations

    public class Solution {
        public int FinalValueAfterOperations(string[] operations) {
            int n = operations.Length;
            int x = 0;
            for (int i = 0; i < n; i++)
            {
                if (operations[i] == "++X" || operations[i] == "X++")
                    x++;
                else if (operations[i] == "--X" || operations[i] == "X--")
                     x--;
            }
            return x;  
        }
    }
    
Concatenation of Array

    public class Solution {
        public int[] GetConcatenation(int[] nums) {
            int[] result = new int[nums.Length * 2];
            for (int i = 0;i < nums.Length; i++)
            {
                result[i] = nums[i];
                result[i + nums.Length] = nums[i];
            }
            return result;
        }
    }
    
Build Array from Permutation

    class Solution {
      List<int> buildArray(List<int> nums) {
        List<int> result = [];
        for(int i = 0; i < nums.length; i++) {
            result.add(nums[nums[i]]);
        }
        return result;
      }
    }
