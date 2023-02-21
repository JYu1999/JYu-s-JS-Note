- [Leetcode 1047](https://leetcode.com/problems/remove-all-adjacent-duplicates-in-string/description/)
	```Javascript
	  var removeDuplicates = function(s) {
	    const stack = [];
	   for (let i = 0; i < s.length; i++) {
	     const cv = s[i];
	     const top = stack[stack.length - 1];
	  
	     // if last element is same as current pop off from stack
	     if (cv === top) stack.pop();
	     else stack.push(cv); // if not equal, add to stack
	   }
	  
	   return stack.join('');
	  };
	  
	  let str = "aacad";
	  
	  console.log(removeDuplicates(str));
	  ```
- [Leetcode 20](https://leetcode.com/problems/valid-parentheses/)
```Javascript
	  var isValid = function(s) {
	      // Initialize stack to store the closing brackets expected...
	      let stack = [];
	      // Traverse each charater in input string...
	      for (let idx = 0; idx < s.length; idx++) {
	          // If open parentheses are present, push it to stack...
	          if (s[idx] == '{') {
	              stack.push('}');
	          } else if (s[idx] == '[') {
	              stack.push(']');
	          } else if (s[idx] == '(') {
	              stack.push(')');
	          }
	          // If a close bracket is found, check that it matches the last stored open bracket
	          else if (stack.pop() !== s[idx]) {
	              return false;
	          }
	      }
	      return !stack.length;
	  };
```