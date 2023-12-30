# $COUNTING$ Rules

## There are two basic rules of counting:
1. Counting by steps ("and" aka "multiply")
    * If you have an experiment with 2 parts, where the first part can be done in $n1$ ways, and the second part can be done in $n2$ ways, then the total number of ways to do the experiment is $n1 * n2$.
    * This is called the **Step Rule** or **Product Rule** of counting.
2. Counting by cases ("or" aka "add")
    * If the outcome of an experiment can either be drawn from a set of $n1$ objects, or from a set of $n2$ objects, and the two sets are disjoint, then the total number of ways to do the experiment is $n1 + n2$.
    * If the two sets are not disjoint, then the total number of ways to do the experiment is $n1 + n2 - n1n2$.
    * This is called the **Case Rule** or **Sum Rule** of counting.


## Below are the counting operations, for given $n$ objects:

### `SORT` $n$ objects
* For this operation, `ORDER` matters!
* The different ways you can sort $n$ objects are called $permutations$.
* The number of $permutations$ of $n$ `DISTINCT` objects is $n!$ (n $factorial$).
    * $\pi(n) = n! = n(n-1)(n-2)...(2)(1)$

* The number of permutations of $n$ objects, where $n1$ are identical, $n2$ are identical, etc. is $n!/(n1!n2!...)$.
    * $\pi(n) = \dfrac{n!}{n_1!n_2!...n_k!}$

### `CHOOSE` $k$ objects from $n$ objects
* For this operation, `ORDER` does _not_ matter!
* The different ways you can select $k$ objects from $n$ objects are called $combinations$.
* The number of $combinations$ of $k$ objects from $n$ objects is $n!/k!(n-k)!$.

    * $\dbinom{n}{k} = {n!} * {1} * \dfrac{1}{k!} * \dfrac{1}{(n-k)!} \implies \dfrac{n!}{k!(n-k)!}$

    * $\dbinom{n}{k} = \dbinom{n}{n-k}$
    * This is the $Binomial Coefficient$.


### `BUCKET` $n$ objects into $r$ buckets
* For `DISTINCT` objects, the number of ways to bucket $n$ objects into $r$ buckets is $r^n$.
    * $r^n = r * r * r * ... * r$
* For `INDISTINCT` objects, the number of ways to bucket $n$ objects into $r$ buckets is $\dfrac{(n+r-1)!}{n!(r-1)!}$
    * The number of ways to distribute $n$ indistinct objects into $r$ buckets is the same as the number of ways to $permutate$ $n+r-1$ objects such that:
        * $n$ are indistinct objects, and 
        * $r-1$ are indistinct dividers
        * Hence - 
            * $\pi(n+r-1) = (n+r-1)! * \dfrac{1}{n!} * \dfrac{1}{(r-1)!} \implies \dfrac{(n+r-1)!}{n!(r-1)!}$

