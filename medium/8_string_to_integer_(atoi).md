```javascript
const myAtoi = (s) => {
	let i = 0,
		sign = 1,
		res = 0;
	while (s[i] === " ") i++;
	if (s[i] === "+" || s[i] === "-") sign = s[i++] === "-" ? -1 : 1;
	while (s[i] >= "0" && s[i] <= "9") {
		res = res * 10 + (s[i++] - "0");
		if (res * sign >= 2147483648) return sign === -1 ? -2147483648 : 2147483647;
	}
	return res * sign;
};
```
