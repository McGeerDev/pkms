202203310802

Status: #core
Tags: [[Core]]

# Pure functions

 For a consistent input the output will remain the same.
- Pure functions do not have ==side effects==[^1]
- Pure functions are stateless
### Example (js)
```javascript
function pureFunction(x){
	return x*x;
}
```

[[determinants]] are pure functions in that for a arbitrary matrix X the determinant det(X) will remain the same every time it is calculated.


---
# References
[^1]: When a function affects state outside of the function's scope.