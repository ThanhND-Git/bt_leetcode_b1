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
