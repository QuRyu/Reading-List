# Haskell 

##### 1. Iteratees, Oleg Kiselyov

Advantage of iteratees over lazy IO and handle IO: both high level abstraction and precise control. Confusion over the `bind` opetion of generalized verison of iteratee. See [Iteratee](http://okmij.org/ftp/Haskell/Iteratee/) for better illustratoin.



##### 2. Retrofiting Linear Types

Lamdba Calculus core for implementing lineary types, their semantics, and applications.  



##### 3. Functional Programming with Overloading and High-order Polymorphism

Gives the reason for using type classes as to achieve restricted polymorphism, and higher-order type in type constructuctors. 

Gives some applications of the combination of type classes and higher-order types. Note that monad transformers could be modeled in a category theory way. 



##### 4. A tutorial on the universality and expressiveness of fold 

How fold can be used to constrcut other recursive functions and the use of fold as proof principle that avoids the need for inductive proofs.  

The universality of fold states the equivalence between fold and recursive programs. The paper also presents various specific aspects of universality, e.g. fusion property 



##### 5. Lazy Functional State Threads

Manipulate named mutable objects in a purely functional way, using the ST monad (the paper did not state it is a monad, though). 

#### *Reread*####  

prerequisite: *Types and Programming Lanaguages*; *Unboxed values as first class citiens* 





##### 6. Concurrent Control with "Readers" and "Writers"

Presents two solutions: 1. the reader has the priority so that as long as there are readers going on, the writer waits indefinitely. 2. the writer has the priority so the reader waits indefinitely. 

Because there must be at most one writer present at a given time, there must be two semaphores for the writer, one for incrementing the count, another for gaining exclusive access to resources. 