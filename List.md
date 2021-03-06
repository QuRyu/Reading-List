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



##### 7. Independent Solutions to Extension Problems 

Presents solutions to extension problems, that is, how to extend software in terms of data and functions while being able to compile the code separately. The dependent type in trait plays an important role such that this type will not be typed until extended by a concrete class. Probably only possible in Scala? 



##### 8. On Understanding Types, Data Abstraction and Polymorphism 

Section 1 gives the history of evolution of types in programming languages and mathematical model (Lambda Caculus, for example). No types exist initially, as the case for Lisp. 

Polymorphism in OOP is a kind of universal polymorphism, so is parametric polymorphism. 



An intuition model for types is given: there is a universe of V of all values. Types are sets in the V universe: the phrase *having a type* is interpreted as *membership in the appropriate set*. 

Thus a monomorphic type system is one in which each value belongs to at most one type. 

A polymorphic type is one in which large collection of values belong to many types. 



##### 9. [Pipes Tutorial](https://hackage.haskell.org/package/pipes-4.3.2/docs/Pipes-Tutorial.html)

Standard intro into the use of Pipes library. No implementation details. 



##### 10. [Coroutines for Steaming](http://www.cs.cornell.edu/courses/cs6110/2013sp/lectures/lec25-sp13.pdf)

Start from the implementation of `Coroutines`. But the implementation differes from that of moand-coroutine library, no idea if it's for illustration or the internal implementaion of the library changed over time. 



##### 11. [Simply Typed Lambda Calculus]( http://www.cs.cornell.edu/courses/cs6110/2013sp/lectures/lec25-sp13.pdf)

Elementary intro notes from Cornell course. 

Cornell added to transfer list LOL. 



##### 12. [Vim Text Objects](http://blog.carbonfive.com/2011/10/17/vim-text-objects-the-definitive-guide/)

Comprehensive guide on the use of vim text objects. 



##### 13. [Scrap Your Type Class](http://www.haskellforall.com/2012/05/scrap-your-type-classes.html)

Implement the type class at data value level, so that no extension would be required, API maintainence would be easier, and programming would even be safer. But only an impossible argument.



##### 14. [Become a Commoand-Line Power User with Oh-My-Zsh and Z](https://www.smashingmagazine.com/2015/07/become-command-line-power-user-oh-my-zsh-z/)

A guide on insalling zsh and oh-my-zsh and related plugins. 



##### 15. [First Class Module without Defaults](http://www.haskellforall.com/2012/07/first-class-modules-without-defaults.html)

Use RecordWilCards extension to manage package imports. Fancy. 



##### 16. Escape from Ivory Tower: the Haskell Journey

It was after the introduction of overloading by Phil Wadler that Rank-N types, GADTs, and other researches were conducted and implemented in Haskell. 

The principle of no side effects was a compromise to lazy evaluation, for the order of execution is rather arbitrary and fucntions like *print* may or may not work. 



17. Comprehending Monads

The conversion between comprehension structure that follows certians laws and monads. This paper uses `join`,`unit` and `map` to define monads. 



18. Monadic Parsing in Haskell

Use monads, specifically the Parser, to parse programs in a modular and combinatorial way. 

No problem in comprehending the text this time. 



19. [Why constraints on data type are bad](https://stackoverflow.com/questions/24465586/why-constraints-on-data-are-a-bad-thing)

Constrats on data type make it incompitable with type families that do not have the kind of constraints on their instances. For example, any data type with constraints cannot be made instances of `Functor` because functor class do not have type constraints. 

GADTs, however, can be use for one-purpose data types, as using type family would be a over-skill. 



20. [Why Free Monads Matter](http://www.haskellforall.com/2012/06/you-could-have-invented-free-monads.html)

The way free monads are structured and how we can use them. Now I finally understand why Stream library is designed so. 



21. [From Object Algebras to Finally Tagless Interpreters](https://oleksandrmanzyuk.wordpress.com/2014/06/18/from-object-algebras-to-finally-tagless-interpreters-2/)

Essentially the implementation of the paper *Independent Solutions to Extension Problem* in Java and Haskell. 



22. Into the cores: squeezing Haskell into nine constructos 

Introduction to the intermediate language for Haskell, which is based on System F with a few extensions. The core language is also typed so that after each phase of transformation the types could still be checked against to ensure correctness. This approach has the better advantage that the compiler does not find bugs only after trying to execute the program. 



Subsequent content is similar to the book *The Implementation of Functional Languages*. Without slides it is almost impossible to see the code. 



23. [Managing Data Classes with Ids](http://blog.originate.com/blog/2015/04/06/managing-data-classes-with-ids/)

The way data should be represented when each data object from the same case class may or may not have a data field (in the blog this field is id) — wrap the object with another layer which adds the optional data field. 



24. [What We Talk About When We Talk About DIstributed Systems](http://alvaro-videla.com/2015/12/learning-about-distributed-systems.html)

Explains each concept of distributed systems, with resources for studying specific topic. Great reference and guide. 



25. Immutability Changes Everything 

With increasing and cheaper storage, it is possible to change everything at every software layer into immutable form. This paper gives several examples, ranging from bank accountants to hardware. 



26. [How Haskell handles parallel computing on a multicore machine/cluster](https://stackoverflow.com/questions/44393439/how-haskell-handles-parallel-computing-on-a-multicore-machine-cluster)

Evaluation of Haskell for concurrent and distributed systems. 



27. [Why there is no implicit parallelism in Haskell](https://stackoverflow.com/questions/15005670/why-is-there-no-implicit-parallelism-in-haskell)

The problem is with granularity. Too fine a particle results in huge overhead, while too coarse one a waste of CPUs. Creating threads casually puts burden on memory and GC, and letting the compiler figure out the right amount of parallelism amounts to solving halting problem. 