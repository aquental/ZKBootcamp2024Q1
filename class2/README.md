## Class 2 - Feb 20

[Lesson](./Lesson2.pdf)

[Homework](./Homework2.pdf)

---

### [Zokrates](https://github.com/Zokrates/ZoKrates)

[Creating simple zero-knowledge verifier contract with ZoKrates (0.7.13) solidity (0.8.0)](https://andresaaap.medium.com/creating-simple-zero-knowledge-verifier-contract-with-zokrates-0-7-13-solidity-0-8-0-666518e1f411)

## [Zokrates](https://zokrates.github.io/)

### [Getting started](https://zokrates.github.io/gettingstarted.html)

### [Zokrates playground](https://play.zokrat.es/)

```zokrates
//Example from Zokrates
// square
def main(private field a, field b) {
    assert (a*a == b);
    return;
}
```

```zokrates
// conditionals
def main(field x) -> field {
    field y = if x + 2 == 3 { 1 } else { 5 };
    return y;
}
```

```zokrates
// loops
def main() -> u32 {
    u32 mut res = 0;
    for u32 i in 0..4 {
        for u32 j in i..5 {
            res = res + i;
        }
    }
    return res;
}
```

```zokrates
// functions
def foo(field a, field b) -> field {
    return a + b;
}

def main() -> field {
    return foo(1, 2);
}
```

```zokrates
// generics
def sum<N>(field[N] a) -> field {
    field mut res = 0;
    for u32 i in 0..N {
        res = res + a[i];
    }
    return res;
}

def main(field[3] a) -> field {
    return sum(a);
}

// Merkle Tree
import "hashes/sha256/512bit" as hash;
import "hashes/utils/256bitsDirectionHelper" as multiplex;

const u32 DEPTH = 3;

def select(bool condition, u32[8] left, u32[8] right) -> (u32[8], u32[8]) {
    return (condition ? right : left, condition ? left : right);
}

// Merke-Tree inclusion proof for tree depth 3 using sha256
// directionSelector => true if current digest is on the rhs of the hash
def main(u32[8] root, private u32[8] leaf, private bool[DEPTH] directionSelector, private u32[DEPTH][8] path) -> bool {
    // Start from the leaf
    u32[8] mut digest = leaf;

	// Loop up the tree
    for u32 i in 0..DEPTH {
	    (u32[8], u32[8]) s = select(directionSelector[i], digest, path[i]);
	    digest = hash(s.0, s.1);
    }

    return digest == root;
}
```

---

# **_Homework Maths_**

1.  Modular arithmetic - you just need to find examples, you don't need to prove anything.

- Is it true that all odd squares are ≡ 1 (mod 8) ?
  > yes : [Prove that odd perfect square is congruent to 1 modulo 8](https://math.stackexchange.com/questions/268402/prove-that-odd-perfect-square-is-congruent-to-1-modulo-8#:~:text=Since%20every%20odd%20integer%20is,squared%20is%201%20mod%208.)
- what about even squares (mod 8) ?
  > yes : [square modulo 8](https://proofwiki.org/wiki/Square_Modulo_8)

1. What do you understand by

- O(n):
  > **linear time** [O(n)](<https://en.wikipedia.org/wiki/O(n)>)
- O(1):
  > **constant time** [O(1)](https://en.wikipedia.org/wiki/Time_complexity#Constant_time)
- O(log n):
  > **logaritmic time** [O(log n)](https://en.wikipedia.org/wiki/Time_complexity#Logarithmic_time)

3. For a proof size, which of these would you want ?
   > _O(1)_ **constant time**
