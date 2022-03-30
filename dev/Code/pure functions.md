# Pure Functions
- For a consistent input the output will remain the same.
- Pure functions do not have ==side effects==[^1]
- Pure functions are stateless
### Example (js)
```javascript
function pureFunction(x){
	return x*x;
}
```

[^1]: When a function affects state outside of the function's scope.