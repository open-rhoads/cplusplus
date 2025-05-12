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
**The above algorithm has a space complexity of O(N) because it creates a new array called collection to store each element of the array that is passed to it.**
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
**Instead of using a new array, we can modify the original array as follows:**
```javascript
function reverse(array) {
    for (let i = 0; i < Math.floor(array.length / 2); i++) {
        let temp = array[i];
        array[i] = array[array.length - 1 - i];
        array[array.length - 1 - i] = temp;
    }
    return array;
}

```
**The above algorithm has a space complexity of O(N) because it also creates a new array in which to store the reversed array**
## Number 3
Create a new function to reverse an array that takes up just O(1) extra space.
```javascript
function reverse(array) { 
		for (let i = array.length - 1; i >= 0; i--) { // loop through the array from back to front
			
				// array.push(array[i]);
		}
		return array;
}
```
**The above function will take only O(1) space complexity because instead of creating a new array in which to store the reversed array,**
## Number 4
Fill in the table that follows to describe the efficiency of a function that accepts an array of numbers and returns an array containing those numbers multiplied by 2 in terms of both time and space:
### Example 1
```javascript
function doubleArray1(array) { 
	let newArray = [];

	for(let i = 0; i < array.length; i++) { 
		newArray.push(array[i] * 2);
	}
	return newArray; 
}
```
### Example 2
```javascript
function doubleArray2(array) {
	for(let i = 0; i < array.length; i++) {
  	array[i] *= 2;
  }
	return array; 
}
```
### Example 3
```javascript
function doubleArray3(array, index=0) { 
	if (index >= array.length) { return; }
  array[index] *= 2;
  doubleArray3(array, index + 1);
	return array; 
}
```
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
