# Codewars JavaScript Solutions

---

## Complementary DNA

Deoxyribonucleic acid (DNA) is a chemical found in the nucleus of cells and carries the "instructions"
for the development and functioning of living organisms.

If you want to know more: http://en.wikipedia.org/wiki/DNA

In DNA strings, symbols "A" and "T" are complements of each other, as "C" and "G".
Your function receives one side of the DNA (string, except for Haskell);
you need to return the other complementary side.
DNA strand is never empty or there is no DNA at all (again, except for Haskell).

More similar exercise are found here: http://rosalind.info/problems/list-view/ (source)

Example: (input --> output)

"ATTGC" --> "TAACG"
"GTAT" --> "CATA"

### Solution 1

```

function DNAStrand(dna) {
  dna = dna.split("");
  let newDna = dna.map((char) => {
    if (char == "A") {
      return (char = "T");
    } else if (char == "T") {
      return (char = "A");
    } else if (char == "C") {
      return (char = "G");
    } else if (char == "G") {
      return (char = "C");
    }
  });
  return newDna.join("");
}
```

### Solution 2

```
      function DNAStrand(dna) {
        let newDna = "";

        for (let i = 0; i <= dna.length - 1; i += 1) {
          if (dna[i] === "A") {
            newDna += "T";
          } else if (dna[i] === "T") {
            newDna += "A";
          } else if (dna[i] === "C") {
            newDna += "G";
          } else {
            newDna += "C";
          }
        }

        return newDna;
      }
```
