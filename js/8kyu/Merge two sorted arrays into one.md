# Codewars JavaScript Solutions

---

## Merge two sorted arrays into one

You are given two sorted arrays that both only contain integers.
Your task is to find a way to merge them into a single one, sorted in asc order.
Complete the function mergeArrays(arr1, arr2), where arr1 and arr2 are the original sorted arrays.
You don't need to worry about validation, since arr1 and arr2 must be arrays with 0 or more Integers.
If both arr1 and arr2 are empty, then just return an empty array.
Note: arr1 and arr2 may be sorted in different orders. Also arr1 and arr2 may have same integers.
Remove duplicated in the returned result.

Examples (input -> output)
`[1, 2, 3, 4, 5], [6, 7, 8, 9, 10] -> [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`
`[1, 3, 5, 7, 9], [10, 8, 6, 4, 2] -> [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`

### Solution #1

```
function mergeArrays(arr1, arr2) {
 for (let i = 0; i <= arr2.length - 1; i += 1) {
   if (!arr1.includes(arr2[i])) {
     arr1.push(arr2[i]);
   }
 }
 return arr1.sort((a, b) => a - b);
}
```

### Solution #2

```
function mergeArrays(arr1, arr2) {
  let arr = [...arr1, ...arr2];
  let newArr = [];

  for (let i = 0; i < arr.length; i += 1) {
    if (!newArr.includes(arr[i])) {
      newArr.push(arr[i]);
    }
  }
  return newArr.sort((a, b) => a - b);
}

```
