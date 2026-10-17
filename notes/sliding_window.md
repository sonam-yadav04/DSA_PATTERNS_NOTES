## 424. Longest Repeating Character Replacement

**Pattern:** Variable-size Sliding Window + Frequency Map

**Recognition clue:** Find the longest substring that can be made of one repeating character by replacing at most `k` characters.

**Core idea:**
- Expand the window by moving `right`.
- Track character frequencies and the maximum frequency in the window.
- Replacements needed = `window length - max frequency`.
- If replacements needed exceed `k`, shrink the window from the left.
- Track the maximum valid window length.

**Key formula:**

`replacements = (right - left + 1) - max_frequency`

**Remember:** Keep the most frequent character unchanged; replace the other characters.

**Common mistake:** Forgetting that `max_frequency` may remain unchanged when the window shrinks. This is valid for the standard optimized sliding-window approach.

**Complexity:** O(n) time, O(1) space for the fixed 26-letter uppercase English alphabet.