```javascript
const convert = (s, numRows) => {
	if (numRows === 1) return s;
	const zigzag = Array.from({ length: numRows }, () => []);
	let row = 0,
		dir = -1;
	for (const char of s) {
		zigzag[row].push(char);
		if (row === 0 || row === numRows - 1) dir *= -1;
		row += dir;
	}
	return zigzag.flat().join("");
};
```
