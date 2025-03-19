# Contents

* [Cover](.)
* [Forward](forward)
* [Preface to the Second Edition](pref-2)
* [Preface to the First Edition](pref-1)
* [Acknowledgments](ack)

---
* [1 Building Abstractions with Procedures](chap-1)
    * [1.1 The Elements of Programming](chap-1#11)
        * [1.1.1 Expressions](chap-1#111)
        * [1.1.2 Naming and the Environment](chap-1#112)
        * [1.1.3 Evaluating Combinations](chap-1#113)
        * [1.1.4 Compound Procedures](chap-1#114)
        * [1.1.5 The Substitution Model for Procedure Application](chap-1#115)
        * [1.1.6  Conditional Expressions and Predicates](chap-1#116)
        * [1.1.7  Example: Square Roots by Newton's Method](chap-1#117)
        * [1.1.8  Procedures as Black-Box Abstractions](chap-1#118)
    * [1.2  Procedures and the Processes They Generate](chap-1#12)
        * [1.2.1  Linear Recursion and Iteration](chap-1#121)
        * [1.2.2  Tree Recursion](chap-1#122)
        * [1.2.3  Orders of Growth](chap-1#123)
        * [1.2.4  Exponentiation](chap-1#124)
        * [1.2.5  Greatest Common Divisors](chap-1#125)
        * [1.2.6  Example: Testing for Primality](chap-1#126)
    * [1.3  Formulating Abstractions with Higher-Order Procedures](chap-1#13)
        * [1.3.1  Procedures as Arguments](chap-1#131)
        * [1.3.2  Constructing Procedures Using Lambda](chap-1#132)
        * [1.3.3  Procedures as General Methods](chap-1#133)
        * [1.3.4  Procedures as Returned Values](chap-1#134)

* [2  Building Abstractions with Data](chap-2)
    * [2.1  Introduction to Data Abstraction](chap-2#21)
        * [2.1.1  Example: Arithmetic Operations for Rational Numbers](chap-2#211)
        * [2.1.2  Abstraction Barriers](chap-2#212)
        * [2.1.3  What Is Meant by Data?](chap-2#213)
        * [2.1.4  Extended Exercise: Interval Arithmetic](chap-2#214)
    * [2.2  Hierarchical Data and the Closure Property](chap-2#22)
        * [2.2.1  Representing Sequences](chap-2#221)
        * [2.2.2  Hierarchical Structures](chap-2#222)
        * [2.2.3  Sequences as Conventional Interfaces](chap-2#223)
        * [2.2.4  Example: A Picture Language](chap-2#224)
    * [2.3  Symbolic Data](chap-2#23)
        * [2.3.1  Quotation](chap-2#231)
        * [2.3.2  Example: Symbolic Differentiation](chap-2#232)
        * [2.3.3  Example: Representing Sets](chap-2#233)
        * [2.3.4  Example: Huffman Encoding Trees](chap-2#234)
    * [2.4  Multiple Representations for Abstract Data](chap-2#24)
        * [2.4.1  Representations for Complex Numbers](chap-2#241)
        * [2.4.2  Tagged data](chap-2#242)
        * [2.4.3  Data-Directed Programming and Additivity](chap-2#243)
    * [2.5  Systems with Generic Operations](chap-2#25)
        * [2.5.1  Generic Arithmetic Operations](chap-2#251)
        * [2.5.2  Combining Data of Different Types](chap-2#252)
        * [2.5.3  Example: Symbolic Algebra](chap-2#253)

* [3  Modularity, Objects, and State](chap-3)
    * [3.1  Assignment and Local State](chap-3#31)
        * [3.1.1  Local State Variables](chap-3#311)
        * [3.1.2  The Benefits of Introducing Assignment](chap-3#312)
        * [3.1.3  The Costs of Introducing Assignment](chap-3#313)
    * [3.2  The Environment Model of Evaluation](chap-3#32)
        * [3.2.1  The Rules for Evaluation](chap-3#321)
        * [3.2.2  Applying Simple Procedures](chap-3#323)
        * [3.2.3  Frames as the Repository of Local State](chap-3#323)
        * [3.2.4  Internal Definitions](chap-3#324)
    * [3.3  Modeling with Mutable Data](chap-3#33)
        * [3.3.1  Mutable List Structure](chap-3#331)
        * [3.3.2  Representing Queues](chap-3#332)
        * [3.3.3  Representing Tables](chap-3#333)
        * [3.3.4  A Simulator for Digital Circuits](chap-3#334)
        * [3.3.5  Propagation of Constraints](chap-3#335)
    * [3.4  Concurrency: Time Is of the Essence](chap-3#34)
        * [3.4.1  The Nature of Time in Concurrent Systems](chap-3#341)
        * [3.4.2  Mechanisms for Controlling Concurrency](chap-3#342)
    * [3.5  Streams](chap-3#35)
        * [3.5.1  Streams Are Delayed Lists](chap-3#351)
        * [3.5.2  Infinite Streams](chap-3#352)
        * [3.5.3  Exploiting the Stream Paradigm](chap-3#353)
        * [3.5.4  Streams and Delayed Evaluation](chap-3#354)
        * [3.5.5  Modularity of Functional Programs and Modularity of Objects](chap-3#355)

* 4  Metalinguistic Abstraction
    * 4.1  The Metacircular Evaluator
        * 4.1.1  The Core of the Evaluator
        * 4.1.2  Representing Expressions
        * 4.1.3  Evaluator Data Structures
        * 4.1.4  Running the Evaluator as a Program
        * 4.1.5  Data as Programs
        * 4.1.6  Internal Definitions
        * 4.1.7  Separating Syntactic Analysis from Execution
    * 4.2  Variations on a Scheme -- Lazy Evaluation
        * 4.2.1  Normal Order and Applicative Order
        * 4.2.2  An Interpreter with Lazy Evaluation
        * 4.2.3  Streams as Lazy Lists
    * 4.3  Variations on a Scheme -- Nondeterministic Computing
        * 4.3.1  Amb and Search
        * 4.3.2  Examples of Nondeterministic Programs
        * 4.3.3  Implementing the Amb Evaluator
    * 4.4  Logic Programming
        * 4.4.1  Deductive Information Retrieval
        * 4.4.2  How the Query System Works
        * 4.4.3  Is Logic Programming Mathematical Logic?
        * 4.4.4  Implementing the Query System

* 5  Computing with Register Machines
    * 5.1  Designing Register Machines
        * 5.1.1  A Language for Describing Register Machines
        * 5.1.2  Abstraction in Machine Design
        * 5.1.3  Subroutines
        * 5.1.4  Using a Stack to Implement Recursion
        * 5.1.5  Instruction Summary
    * 5.2  A Register-Machine Simulator
        * 5.2.1  The Machine Model
        * 5.2.2  The Assembler
        * 5.2.3  Generating Execution Procedures for Instructions
        * 5.2.4  Monitoring Machine Performance
    * 5.3  Storage Allocation and Garbage Collection
        * 5.3.1  Memory as Vectors
        * 5.3.2  Maintaining the Illusion of Infinite Memory
    * 5.4  The Explicit-Control Evaluator
        * 5.4.1  The Core of the Explicit-Control Evaluator
        * 5.4.2  Sequence Evaluation and Tail Recursion
        * 5.4.3  Conditionals, Assignments, and Definitions
        * 5.4.4  Running the Evaluator
    * 5.5  Compilation
        * 5.5.1  Structure of the Compiler
        * 5.5.2  Compiling Expressions
        * 5.5.3  Compiling Combinations
        * 5.5.4  Combining Instruction Sequences
        * 5.5.5  An Example of Compiled Code
        * 5.5.6  Lexical Addressing
        * 5.5.7  Interfacing Compiled Code to the Evaluator
