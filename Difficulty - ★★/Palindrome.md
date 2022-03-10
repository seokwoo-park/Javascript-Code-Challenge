# Available books

## Difficulty ★★☆☆☆ (_Completed_)

### Summary

> is a word, phrase, number, or other sequence of characters which reads the same backward or forward.

### Solution

```typescript
function isPalindrome(str: string) {
  str = str.toLocaleLowerCase();
  const reverse = str.split("").reverse().join("");

  str === reverse ? console.log("Palindrome!") : false;
}

isPalindrome("racecar"); // OUTPUT: "Palindrome!"
isPalindrome("car"); // False
```
