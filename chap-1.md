# Chapter 1
# Building Abstractions with Procedures
<script src="snapblocks.min.js"></script>


> The acts of the mind, wherein it exerts its power over simple ideas, are chiefly these three: 1. Combining 
> several simple ideas into one compound one, and thus all complex ideas are made. 2. The second is bringing 
> two ideas, whether simple or complex, together, and setting them by one another so as to take a view of 
> them at once, without uniting them into one, by which it gets all its ideas of relations. 3. The third is 
> separating them from all other ideas that accompany them in their real existence: this is called 
> abstraction, and thus all its general ideas are made.

~ John Locke, An Essay Concerning Human Understanding (1690)


We are about to study the idea of a computational process. Computational processes are abstract beings that inhabit computers. As they evolve, processes manipulate other abstract things called data. The evolution of a process is directed by a pattern of rules called a program. People create programs to direct processes. In effect, we conjure the spirits of the computer with our spells.

A computational process is indeed much like a sorcerer's idea of a spirit. It cannot be seen or touched. It is not composed of matter at all. However, it is very real. It can perform intellectual work. It can answer questions. It can affect the world by disbursing money at a bank or by controlling a robot arm in a factory. The programs we use to conjure processes are like a sorcerer's spells. They are carefully composed from symbolic expressions in arcane and esoteric programming languages that prescribe the tasks we want our processes to perform.

A computational process, in a correctly working computer, executes programs precisely and accurately. Thus, like the sorcerer's apprentice, novice programmers must learn to understand and to anticipate the consequences of their conjuring. Even small errors (usually called bugs or glitches) in programs can have complex and unanticipated consequences.

Fortunately, learning to program is considerably less dangerous than learning sorcery, because the spirits we deal with are conveniently contained in a secure way. Real-world programming, however, requires care, expertise, and wisdom. A small bug in a computer-aided design program, for example, can lead to the catastrophic collapse of an airplane or a dam or the self-destruction of an industrial robot.

Master software engineers have the ability to organize programs so that they can be reasonably sure that the resulting processes will perform the tasks intended. They can visualize the behavior of their systems in advance. They know how to structure programs so that unanticipated problems do not lead to catastrophic consequences, and when problems do arise, they can debug their programs. Well-designed computational systems, like well-designed automobiles or nuclear reactors, are designed in a modular manner, so that the parts can be constructed, replaced, and debugged separately.


## Programming in Snap<i>!</i>
We need an appropriate language for describing processes, and we will use for this purpose the programming language [Snap<i>!</i>](http://snap.berkeley.edu/run). Just as our everyday thoughts are usually expressed in our natural language (such as English, French, or Japanese), and descriptions of quantitative phenomena are expressed with mathematical notations, our procedural thoughts will be expressed in Snap<i>!</i>. Snap<i>!</i> was invented around 2008 as a modification of Scratch that added recursion equations, making it more suitable for college students. The language was conceived by Jens Mönig and Brian Harvey, and is documented in Dr. Harvey's paper, ["Why do we Need to Learn this Baby Language?"](https://people.eecs.berkeley.edu/~bh/snap/baby3.pdf) (Harvey 2019)

Despite its inception as a mod of Scratch, Snap<i>!</i> is its own language. Modern Snap<i>!</i> was rewritten from the ground up. Snap<i>!</i> is maintained almost exclusively by Jens Mönig, with the cloud storage systems maintained by a small team and paid for by him.  Snap<i>!</i> was designed to provide symbol-manipulating capabilities for attacking programming problems such as the symbolic differentiation and integration of algebraic expressions. It included for this purpose new first-class lists and blocks, which set it apart from most other block-based languages.

If Snap<i>!</i> is not a mainstream language, why are we using it as the framework for our discussion of programming? Because the language possesses unique features that make it an excellent medium for studying important programming constructs and data structures and for relating them to the linguistic features that support them. The most significant of these features is the fact that Snap<i>!</i> descriptions of processes, called procedures, can themselves be represented and manipulated as Snap<i>!</i> data. The importance of this is that there are powerful program-design techniques that rely on the ability to blur the traditional distinction between ''passive'' data and ''active'' processes. As we shall discover, Snap<i>!</i>'s flexibility in handling procedures as data makes it one of the most convenient languages in existence for exploring these techniques. The ability to represent procedures as data also makes Snap<i>!</i> an excellent language for writing programs that must manipulate other programs as data, such as the interpreters and compilers that support computer languages. Above and beyond these considerations, programming in Snap<i>!</i> is great fun.

## 1.1
## The Elements of Programming

A powerful programming language is more than just a means for instructing a computer to perform tasks. The language also serves as a framework within which we organize our ideas about processes. Thus, when we describe a language, we should pay particular attention to the means that the language provides for combining simple ideas to form more complex ideas. Every powerful language has three mechanisms for accomplishing this:


* primitive expressions, which represent the simplest entities the language is concerned with,
* means of combination, by which compound elements are built from simpler ones, and
* means of abstraction, by which compound elements can be named and manipulated as units.

In programming, we deal with two kinds of elements: procedures and data. (Later we will discover that they are really not so distinct.) Informally, data is ''stuff'' that we want to manipulate, and procedures are descriptions of the rules for manipulating the data. Thus, any powerful programming language should be able to describe primitive data and primitive procedures and should have methods for combining and abstracting procedures and data.

In this chapter we will deal only with simple numerical data so that we can focus on the rules for building procedures. In later chapters we will see that these same rules allow us to build procedures to manipulate compound data as well.

### 1.1.1
### Expressions
One easy to get started at programming is to examine some typical interactions with Snap<i>!</i>. Imagine that you are sitting at a computer. You drag together an *expression*, and the interpreter responds by displaying the result of its *evaluating* that expression.

One kind of primitive expression you might type is a number. (More precisely, the expression that you type consists of the numerals that represent the number in base 10.) If you present Snap<i>!</i> with a number

<pre class=blocks>
((486) + () $<:>)
</pre>

the interpreter will respond by printing

*486*

Expressions representing numbers may be combined with an expression representing a primitive procedure (such as + or *) to form a compound expression that represents the application of the procedure to those numbers. For example:

<pre class=blocks>
((137) + (349) $<:>) //486
((1000) - (334)) //666
((5) * (99) $<:>) //495
((10) / (5)) //2
((2.7) + (10) $<:>) //12.7
</pre>

Expressions such as these, formed by delimiting values inside a block, are called combinations. The block is also called the *operator*, and the other elements are called *operands*. The value of a combination is obtained by applying the procedure specified by the operator to the *arguments* that are the values of the operands.

The convention of making the operator be represented is very useful partially because it can accommodate procedures that may take an arbitrary number of arguments, as in the following examples:

<pre class=blocks>
((21) + (35) + (12) + (7) $<:>) //75

((25) * (4) * (12) $<:>) //1200
</pre>
No ambiguity can arise, because the operator is always the outermost block. (You can obtain these multi-input variants by clicking the little arrows on the right edge of the block)

A second advantage of of this notation is that it extends in a straightforward way to allow combinations to be nested, that is, to have combinations whose elements are themselves combinations:

<pre class=blocks>
(((3) * (5) $<:>) + ((10) - (6)) $<:>) //19
</pre>

There is no limit (in principle) to the depth of such nesting and to the overall complexity of the expressions that the Snap<i>!</i> interpreter can evaluate. It is we humans who get confused by still relatively simple expressions such as

<pre class=blocks>
(((3) * (((2) * (4) $<:>) + (3) + (5) $<:>) $<:>) + ((10) - (7)) + (6) $<:>)
</pre>

which the interpreter would readily evaluate to be 57. Luckily, Snap<i>!</i> uses a feature called *zebra striping*, where blocks alternate between light and dark, to help us keep track of the nesting of blocks.

Even with complex expressions, the interpreter always operates in the same basic cycle: it detects when the user clicks a block, evaluates the expression, and prints the result. This mode of operation is often expressed by saying that the interpreter runs in a *read-eval-print loop*. Observe in particular that it is not necessary to explicitly instruct the interpreter to print the value of the expression.

### 1.1.2
### Naming and the Environment
A critical aspect of a programming language is the means it provides for using names to refer to computational objects. We say that the name identifies a *variable* whose *value* is the object.

In the Scheme dialect of Lisp, we name things with the ![Make a variable](variable.png) button (found in the "Variables" category). Creating a variable <code class=block>(size :: variables)</code> and running <code class=block>set [size V] to [2]</code> causes the interpreter to associate the value 2 with the name size. Once the name size has been associated with the number 2, we can refer to the value 2 by name:

<pre class=blocks>
(size :: variables) //2
((5) * (size :: variables) $<:>) // 10
</pre>

Here are further examples of the use of <code class=block>set [ V] to []</code>:

<pre class=blocks>
set [tau V] to [6.283185]

set [radius V] to [10]

( (0.5) * ((tau) * (radius) $<:>) * (radius) $<:>) // 314.159

set [circumference V] to ((tau) * (radius) $<:>)

(circumference) //62.8318
</pre>
![Make a variable](variable.png) and <code class=block>set [ V] to []</code> are our language's simplest means of abstraction, for it allows us to use simple names to refer to the results of compound operations, such as the <code class=block>(circumference)</code> computed above. In general, computational objects may have very complex structures, and it would be extremely inconvenient to have to remember and repeat their details each time we want to use them. Indeed, complex programs are constructed by building, step by step, computational objects of increasing complexity. The interpreter makes this step-by-step program construction particularly convenient because name-object associations can be created incrementally in successive interactions. This feature encourages the incremental development and testing of programs and is largely responsible for the fact that a Snap<i>!</i> program usually consists of a large number of relatively simple procedures.

It should be clear that the possibility of associating values with symbols and later retrieving them means that the interpreter must maintain some sort of memory that keeps track of the name-object pairs. This memory is called the *environment* (more precisely the *global environment*, since we will see later that a computation may involve a number of different environments).

### 1.1.3
### Evaluating Combinations

One of our goals in this chapter is to isolate issues about thinking procedurally. As a case in point, let us consider that, in evaluating combinations, the interpreter is itself following a procedure.

* To evaluate a combination, do the following:
    1. Evaluate the subexpressions of the combination
    2. Apply the procedure (that is the block) to the arguments that are the values of the other subexpressions (the operands)

Even this simple rule illustrates some important points about processes in general. First, observe that the first step dictates that in order to accomplish the evaluation process for a combination we must first perform the evaluation process on each element of the combination. Thus, the evaluation rule is *recursive* in nature; that is, it includes, as one of its steps, the need to invoke the rule itself.



[Contents](contents) | Previous: [Acknowledgments of the Snap<i>!</i> Edition](ack-snap)

<script>
snapblocks.renderMatching('pre.blocks', {
  wrap:          true,
  zebraColoring: true,
  showSpaces:    true,
});
</script>
<script>
snapblocks.renderMatching('code.block', {
  wrap:          true,
  zebraColoring: true,
  showSpaces:    true,
  inline:        true,
});
</script> 