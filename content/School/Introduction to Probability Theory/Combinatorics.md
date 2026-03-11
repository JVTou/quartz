---
date created: Friday, February 28th 2025, 12:01:01 pm
date modified: Tuesday, February 24th 2026, 9:25:27 pm
---

Counting the number of ways you can pick $k$ objects from a collection of $n$ objects.

# Permutation

The order in which the objects are picked matters. In this case, we call the number of distinct orderings of the $k$ items which are drawn from the collection of $n$ items without replacement the **permutation number**.

$$
P_{n,k}=\frac{n!}{(n-k)!}
$$

## Examples
- Finding the number of ways you can shelve 10 books with only 5 spots
- Finding the number of possible president and vice-president combinations in a class of students
# Combination

The order in which we pick the objects does not matter. In this case, we call the number of distinct orderings of the $k$ items which are drawn from the collection of $n$ items without replacement the **combination number**. This number is similar to the permutation number, but accounts for repetition of collections whose order is different but elements are the same.

$$
C_{n,k}=\frac{P_{n,k}}{k!}=\frac{n!}{k!(n-k)!}
$$

We note the combination number $C_{n,k}={n \choose k}$

## Examples
- The number of full houses that can be dealt from a deck of 52 cards
- The number of four-of-a-kinds that can be dealt in a five card deal from a 52 card deck
