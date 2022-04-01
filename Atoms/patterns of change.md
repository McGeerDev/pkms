202204011651

Status: #idea 
Tags: [[thinking patterns]]

# patterns of change

How to look at a system by the [[observational pattern]] to predict an unknown state in a series

![[Pasted image 20220401165322.png]]

#### System: Trees growing
Looks like [[recursion]]

#### Observations
| Tree number | Number of branches | Number of edges | Color |
| ----------------- | --------------------------- | ----------- | --------|
| 1 | 2 | 2 | black |
| 2 | 6 | 4 | black | 
| 3 | 14 | 8 | black | 
| **4** | ? | ? | black |
| prediction | 30 | 16 | black | 

The  number of branches grows by adding the previous number of edges to the previous number of branches. 
Solving the prediction problem programatically.
```typescript 
const numberOfBranches: number[] = [2];
const numberOfEdges: number[] = [2];
const arrlength = numberOfBranches.lenght;

for i = 1; i < arrlength; i++
	numberOfEdges[i] = 2 * numberOfEdges[i - 1];
	numberOfBranches[index] = numberOfBranches[i - 1] + numberOfEdges


```

#### Things I missed
The thickness of the branches
Amount of limbs

---

## Links

https://www.youtube.com/watch?v=hgybyr9myjg

