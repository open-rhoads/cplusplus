# Space Constraints
The following exercises demonstrate the complexities involved with space constraints.
## Assignment Video
Here is my video explaining this assignment:
## Number 1
Describe the space complexity of the 'Word Builder' algorithm in terms of Big O:
```javascript
function wordBuilder(array) { 
		let collection = [];
		for(let i = 0; i < array.length; i++) { 
				for(let j = 0; j < array.length; j++) {
						if (i !== j) {
								collection.push(array[i] + array[j]);
						}
				}
		}
		return collection; 
}
```
The above algorithm has a space complexity of O(N) because it creates a new array called collection to store each element of the array that is passed to it. 
## Number 2
Describe the space complexity of the following function that reverses an array in terms of Big O:
```javascript
function reverse(array) { 
		let newArray = [];
		for (let i = array.length - 1; i >= 0; i--) { 
				newArray.push(array[i]);
		}
		return newArray;
}
```
## Number 3
Create a new function to reverse an array that takes up just O(1) extra space.
```javascript

```
## Number 4
Fill in the table that follows to describe the efficiency of a function that accepts an array of numbers and returns an array containing those numbers multiplied by 2 in terms of both time and space:

<table>
  <thead>
    <tr>
      <th>Version</th>
      <th>Time Complexity</th>
      <th>Space Complexity</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td></td>
    </tr>
    <tr>
      <td>2</td>
      <td></td>
    </tr>
    <tr>
      <td>3</td>
      <td></td>
    </tr>
  </tbody>
</table>
