202203310801

Status: #Snippet
Tags: [[snippets]]

- Create an [asynchronous](async-await.md) arrow function
```typescript 
const functionName = async () => {}
```

- Creates a generic function with the same type as input and output [[builder-pattern]]
```typescript
const functionName<Type> = (args: Type): Type => {
	return args;
}
```

