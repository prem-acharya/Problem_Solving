Question -> Letter Combinations of a Phone Number

Given a string containing digits from 2-9 inclusive, return all possible letter combinations that the number could represent. Return the answer in any order.

A mapping of digits to letters (just like on the telephone buttons) is given below. Note that 1 does not map to any letters.

<img src="https://assets.leetcode.com/uploads/2022/03/15/1200px-telephone-keypad2svg.png"  width="40%" height="20%">

Example 1:
```
Input: digits = "23"
Output: ["ad","ae","af","bd","be","bf","cd","ce","cf"]
```

Example 2:
```
Input: digits = ""
Output: []
```

Example 3:
```
Input: digits = "2"
Output: ["a","b","c"]
```

Constraints:

- 0 <= digits.length <= 4
- digits[i] is a digit in the range ['2', '9'].


C++ Code:
```C++
class Solution {
public:
    vector<string> letterCombinations(string digits) {
        vector<string> result;
        if (digits.empty())
            return result;
        
        vector<string> digitToLetters = {"", "", "abc", "def", "ghi", "jkl", "mno", "pqrs", "tuv", "wxyz"};
        string combination;
        backtrack(digits, digitToLetters, 0, combination, result);
        return result;
    }
    
private:
    void backtrack(const string& digits, const vector<string>& digitToLetters, int index, string& combination, vector<string>& result) {
        if (index == digits.length()) {
            result.push_back(combination);
            return;
        }
        
        int digit = digits[index] - '0';
        const string& letters = digitToLetters[digit];
        for (char letter : letters) {
            combination.push_back(letter);
            backtrack(digits, digitToLetters, index + 1, combination, result);
            combination.pop_back();
        }
    }
};
```
