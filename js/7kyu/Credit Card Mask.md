# Codewars JavaScript Solutions

---

## Credit Card Mask

Usually when you buy something, you're asked whether your credit card number,
phone number or answer to your most secret question is still correct.
However, since someone could look over your shoulder, you don't want that shown on your screen. Instead, we mask it.

Your task is to write a function maskify, which changes all but the last four characters into '#'.

Examples
"4556364607935616" --> "############5616"
"64607935616" --> "#######5616"
"1" --> "1"
"" --> ""

// "What was the name of your first pet?"

"Skippy" --> "##ippy"

"Nananananananananananananananana Batman!"
-->
"####################################man!"

### Solution 1

```
function maskify(cc) {
let mask = "";
for (let i = 0; i <= cc.length - 5; i += 1) {
mask += "#";
}
if (cc.length >= 5) {
return mask + cc.slice(cc.length - 4);
}
return cc;
}
```

### Solution 2

```
     function maskify(cc) {
        if (typeof cc !== "string") {
          cc = cc.toString();
        }
        const str = cc.substring(cc.length, cc.length - 4);
        const newStr = str.padStart(cc.length, "#");

        return newStr;
      }

```
