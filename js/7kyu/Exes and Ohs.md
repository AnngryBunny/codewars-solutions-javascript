# Codewars JavaScript Solutions

---

## Exes and Ohs

Check to see if a string has the same amount of 'x's and 'o's.
The method must return a boolean and be case insensitive. The string can contain any char.

Examples input/output:

XO("ooxx") => true
XO("xooxx") => false
XO("ooxXm") => true
XO("zpzpzpp") => true // when no 'x' and 'o' is present should return true
XO("zzoo") => false

### Solution 1

```
function XO(str) {
let sumX = 0;
let sumO = 0;
let string = str.toLowerCase().split("");
string.forEach((char) => {
if (char === "x") {
return (sumX += 1);
} else if (char === "o") {
return (sumO += 1);
}
});
return sumX === sumO;
}
```

### Solution 2

```
const XO_2 = (str) => {
str = str.toLowerCase().split("");
return (
str.filter((x) => x === "x").length === str.filter((x) => x === "o").length
);
};
```
