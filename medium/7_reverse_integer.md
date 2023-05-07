```javascript
const reverse = (x) => {
	let rev = 0,
		sign = x < 0 ? -1 : 1;
	x = Math.abs(x);
	while (x) {
		let digit = x % 10;
		x = Math.floor(x / 10);
		rev = rev * 10 + digit;
		if (rev > 2 ** 31 - 1 || rev < -(2 ** 31)) return 0;
	}
	return rev * sign;
};
```
