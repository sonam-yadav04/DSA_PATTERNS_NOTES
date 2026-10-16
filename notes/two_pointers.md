### String Compression — LeetCode 443

**Pattern:** Two pointers + consecutive group counting

**Recognition clue:** Compress consecutive repeated characters in-place.

**Core idea:** Read one group of identical characters using i ,loop through in next loop till the char != chars[i] and icrease count, then write the ch = char[j] in chars and increase j ,  check its count (if greater than 1) then we loop through each digit in count and store digit by digit in chars  array.

**Tricky parts:**
- need to process 2 while loops and 3rd for  loop for saperating digits.
- Write multi-digit counts digit by digit need to use for loop on str(count).
- need to return the j pointer.
- j is the main write pointer as well , every thing we will write with j and icrease it ,

**Complexity:** O(n) time | O(1) auxiliary space

**Revision task:** Reimplement from memory without opening the solution.