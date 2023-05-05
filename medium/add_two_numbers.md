```javascript
const addTwoNumbers = (l1, l2) => {
  let carry = 0;
  const dummyHead = new ListNode(0);
  let curr = dummyHead;

  for (; l1 || l2 || carry; l1 = l1?.next, l2 = l2?.next) {
    const val1 = l1?.val ?? 0;
    const val2 = l2?.val ?? 0;
    const sum = val1 + val2 + carry;
    carry = Math.floor(sum / 10);
    curr.next = new ListNode(sum % 10);
    curr = curr.next;
  }

  return dummyHead.next;
};
```
