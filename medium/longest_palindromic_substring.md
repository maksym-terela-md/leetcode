```javascript
const longestPalindrome = (s) => {
  let result = "";
  for (let i = 0; i < s.length; i++) {
    const expandPalindrome = (start, end) => {
      while (start >= 0 && end < s.length && s[start] === s[end]) {
        start--;
        end++;
      }
      const palindrome = s.substring(start + 1, end);
      if (palindrome.length > result.length) {
        result = palindrome;
      }
    };
    expandPalindrome(i, i);
    expandPalindrome(i, i + 1);
  }
  return result;
};
```
