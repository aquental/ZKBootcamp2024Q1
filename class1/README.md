# Class 1 - Feb 19

[Lesson 1](./Lesson1.pdf)

[Homework 1](./Homework1.pdf)

> [Zero Knowledge Cryptography Introduction - Solidity Fridays](https://www.youtube.com/watch?v=Wne3O9P4jkw)
> 
---

# **Home work** for _class 1_

## Maths Introduction

Some modular arithmetic

1. Working with the following set of Integers S = {0,1,2,3,4,5,6}

   What is

   a) 4 + 4

   > = **_2_**

   ```python
   print((4 + 4) % 6)
   ```

   b) 3 x 5

   > = **_3_**

   ```python
   print((3 * 5) % 6)
   ```

   c) what is the inverse of 3 ?

   > **_0.3333333_**

   ```python
   print((1 / 3) % 6)
   ```

2. For S = {0,1,2,3,4,5,6}

   Can we consider 'S' and the operation '+' to be a group ?

   > No
   > conditions to be a _group_:
   >
   > - Closure: addition is not closed within $S$. $2 + 5 = 7$, which is not an element of $S$.
   > - Associativity: addition is associative. $(a + b) + c = a + (b + c)$ for all elements $a$, $b$, and $c$ in $S$.
   > - Identity: there is no identity. An identity element would need to satisfy $a + e = e$ and $e + a = a$ for all elements $a$ in $S$, but no such element exists in $S$.
   > - Inverse: not all elements have inverses in $S$. There is no element $x$ such that $6 + x = 0$.

3. What is

   -13 mod 5 ?

   > **2**

   ```python
   print(-13 % 5)
   ```

4. Polynomials

   For the polynomial $x^{3}-x^{2}+4x-12$

   Find a the positive root ?

   > cannot find only one positive root

   What is the degree of this polynomial ?

   > **_3_** _(highest exponent of the variable)_

## Use cases

In your teams discuss any systems you have used that involved zero knowledge proofs.

> I studied **Starknet**.

Have you seen any applications of zero knowledge proofs other than with a blockchain ?

> An _Anonymous Verifiable Voting_ algorithm (Using ZKPs, eligible voters can prove their right to cast a ballot without revealing their identity).
>
> > [Zero Knowledge Technology as a future of Banking and Verifiable Autonomous Financial Protocols](https://sergey-kozlov.medium.com/zero-knowledge-technology-as-a-future-of-banking-and-verifiable-autonomous-financial-protocols-33c6226ca9fa)
> >
> > [Checks and balances: Machine learning and zero-knowledge proofs](https://a16zcrypto.com/posts/article/checks-and-balances-machine-learning-and-zero-knowledge-proofs/)
> >
> > [3 Real World Applications of Zero Knowledge Proofs](https://www.coinbureau.com/adoption/applications-zero-knowledge-proofs/)

What is to you, the most important feature of zkp technology ?

> The ability to prove something is _TRUE_ without showing the data for the computation.

Think of some use cases of zero knowledge proofs that you would like to see developed.

> Create verifiable and ownable machine learning app.
