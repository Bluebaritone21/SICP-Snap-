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

Despite its inception as a mod of Scratch, Snap<i>!</i> is its own language. Modern Snap<i>!</i> was rewritten from the ground up. Snap<i>!</i> is maintained almost exculsivly by Jens Mönig, with the cloud storage systems maintained by a small team and paid for by him.  Snap<i>!</i> was designed to provide symbol-manipulating capabilities for attacking programming problems such as the symbolic differentiation and integration of algebraic expressions. It included for this purpose new first-class lists and blocks, which set it apart from most other block-based languages.

If Snap<i>!</i> is not a mainstream language, why are we using it as the framework for our discussion of programming? Because the language possesses unique features that make it an excellent medium for studying important programming constructs and data structures and for relating them to the linguistic features that support them. The most significant of these features is the fact that Snap<i>!</i> descriptions of processes, called procedures, can themselves be represented and manipulated as Snap<i>!</i> data. The importance of this is that there are powerful program-design techniques that rely on the ability to blur the traditional distinction between ''passive'' data and ''active'' processes. As we shall discover, Snap<i>!</i>'s flexibility in handling procedures as data makes it one of the most convenient languages in existence for exploring these techniques. The ability to represent procedures as data also makes Snap<i>!</i> an excellent language for writing programs that must manipulate other programs as data, such as the interpreters and compilers that support computer languages. Above and beyond these considerations, programming in Snap<i>!</i> is great fun.

## 1.1
## The Elements of Programming



<script defer>snapblocks.renderMatching('pre.blocks', {
  wrap:          true,              // Optional, defaults to false. This enabled block wrapping
  zebraColoring: true,     // Optional, defaults to false. Enabled zebra coloring
  showSpaces:    true,        // Optional, defaults to false. Shows spaces in inputs
});</script>
<script defer>snapblocks.renderMatching('code.blocks', {
  style:         'snap',       // Optional, defaults to 'snap'.
  languages:     ['en'],       // Optional, defaults to ['en'].
  scale:         1,                // Optional, defaults to 1
  wrap:          true,              // Optional, defaults to false. This enabled block wrapping
  zebraColoring: true,     // Optional, defaults to false. Enabled zebra coloring
  showSpaces:    true,        // Optional, defaults to false. Shows spaces in inputs
  inline:true,
});</scripts> 