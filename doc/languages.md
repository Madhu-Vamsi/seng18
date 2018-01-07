[home](http://tiny.cc/seng18) |
[copyright](https://github.com/txt/seng18/blob/master/LICENSE.md) &copy;2018, tim&commat;menzies.us
<br>
[<img width=900 src="https://raw.githubusercontent.com/txt/seng18/master/img/banner.png">](http://tiny.cc/seng18)<br>
[syllabus](https://github.com/txt/seng18/blob/master/doc/syllabus.md) |
[src](https://github.com/txt/seng18/tree/master/src) |
[submit](http://tiny.cc/seng18give) |
[chat](https://seng18.slack.com/)


______



# The Sapir-Whorf Hypothesis 

From wikipedia:
- The principle of linguistic relativity holds that the structure of a language affects its speakers' world view or cognition. 
- Popularly known as the Sapir–Whorf hypothesis, or Whorfianism, the principle is often defined to include two versions. The strong version says that language determines thought, and that linguistic categories limit and determine cognitive categories, whereas the weak version says that linguistic categories and usage only influence thought and decisions.


Prevelant in computer language design:

- APL programming language originator Kenneth E. Iverson believed that the Sapir–Whorf hypothesis applied to computer languages (without actually mentioning it by name). His Turing award lecture, "Notation as a tool of thought", was devoted to this theme, arguing that more powerful notations aided thinking about computer algorithms.]
- The essays of Paul Graham explore similar themes, such as a conceptual hierarchy of computer languages, with more expressive and succinct languages at the top. TSts Graham,
writing in some language means thinking in that language. 
 -In a 2003 presentation at an open source convention, Yukihiro Matsumoto, creator of the programming language Ruby, said that one of his inspirations for developing the language was the science fiction novel Babel-17, based on the Sapir–Whorf Hypothesis.

So, do some programming languages make us inherently better programmers?

# So Many Languages

New Repos in Github:


![](200~http://ledeprogram.com/wp-content/uploads/2015/11/tumblr_inline_ntur8wickr1tyf03k_1280.png)

How to understand them all? Which is best?

## Hint0: What every language you think is best, you will change your mind

Languages, sorted by tags (in Stackoverflow.com) and lines changed (in Gitbuf)

+ http://langpop.corger.nl

What language will you use next? From
[Empirical Analysis of Programming Language Adoption
Leo A. Meyerovich Ariel Rabkin, OOPSLA 2013](http://sns.cs.princeton.edu/docs/asr-oopsla13.pdf)

![](http://unbox.org/open/trunk/310/14/spring/doc/img/whatsnext.png)

_
## Hint1: They dont matter as much as we thought


A [study](http://macbeth.cs.ucdavis.edu/lang_study.pdf) conducted by computer scientists from UC Davis attempts to settle a long-term debate among developers: does the choice of a programming language impact code quality in a given project? The answer, according to the researchers, is yes, but that impact is very small.

The paper, titled "A Large Scale Study of Programming Languages and Code Quality in Github," analyzed 729 GitHub projects written in 17 different languages with 80 million lines of code and 1.5 million commits. They found that C, C++, JavaScript, Objective-C, PHP and Python tended to have slightly more errors than average, while Clojure, Haskell, Ruby, Scala and TypeScript were less likely than average to have bugs.

However, the report authors caution that the impact of the language choice was "quite small." Other factors, such as the size of the project and the size of the team, had a much bigger impact on code quality.

## Hint2: Most important software component: Peopleware

What determines pace of new code? Great new languages? Or how effective are the programmers?

Clearly both matter. But programmer effectiveness and ability to work in a team is surprisingly
important. The following notes come from
[https://arxiv.org/pdf/1702.07735.pdf](https://arxiv.org/pdf/1702.07735.pdf):

- Consider the systems studied in that paper (see Fig1).
- Consider the goal of predicting how long it takes to close an issue. What factors
  do you think might be important in achieving that goal? **Write them down.**
- Now look at Table II and ithe oines that were actually used in different data sets
  (see Tablv V). **How many of your features were not used here?**
- Look at the decision trees that decide when an issue is going to close (see Fig3).
  **What is missing from these trees?** (hint: see above)


## Hint3: So many `different' and `new' languages, aren't

Programmers are mostly unaware
that that their programs (they use every day) are surrounded by structures.
_And that this is deliberate_ since the point of programming languages is
to write programs and _programs are things that make maths palatable_.

So every programmer is a mathematician (they just do need to know that).
But every programming language _designer_ needs to understand that maths
since it is that maths that defines what is (im)possible in that language.
  
Don't believe it? Well consider this:

+ Anytime you search for a string, you are probably using 
   [regular expressions](http://goo.gl/KASraS), which is a little language that
    specifies finite state machines.
+ Every time anyone tests a program, they usually doodle a finite state
  machine to clarify the intent of the program.
+ Every time anyone compiles a program, they are using type theory
  to explore the range of operations available for the program types.
+ Every time you pass a variable to a procedure/method/function,
  you are using something like
  Alfonzo Church's [lambda calculus](http://en.wikipedia.org/wiki/Lambda_calculus)
  to ensure that all things that use
  that variable access the right contents. 
+ When the first computers were built in the USA, they were written
  by engineers who literally pulled about the book on some
  uber maths called the [Turing machine](http://en.wikipedia.org/wiki/Turing_machine).
  And the Turing machine was created by Church's Ph.D. student, Alan Turing.
  + Any functional programmer uses McCarthy's 1960 memo on
  [Recursive Functions of Symbolic Expressions](http://www-formal.stanford.edu/jmc/recursive/recursive.html) 
  (which is slightly easier to read in 
  [Paul Graham's version](http://languagelog.ldc.upenn.edu/myl/llog/jmc.pdf)
  or in [Peter Norvig's lispy code](http://norvig.com/lispy.html). 
+ Logic programmers literally program in mathematical logic.
+ If you use the _make_ tool, it find the _dependencies_ in your files
  and can run one parallel computation for each separate set.

The syntactic sugar of a program
consists of all the stuff that makes
the language usable:

+ Simplifications of complex processing;
+ Short-cuts to quickly code common idioms (e.g. macros,
  commonly-used control structures, class or function libraries for
  patterns or idioms);
+ Watch dogs that raise alerts if you do something
  wrong.
 
The maths defines what can be done, and what cannot
be done in that language. Such maths includes:

+ Closures
+ Dependencies
+ Logic
+ The predicates of logic programming
+ Functions
+ Objects
+ State machines
+ Etc

And underneath that maths is another layer of uber maths
([Turing machine](http://en.wikipedia.org/wiki/Turing_machine))
 that defines the ultimate limits of all the above. 

____



# My Favorite Langauge: LUA

Still, you can't help having favoriters

Lua

## A single data structure

There are few fundamental types in Lua and only one of them is designed to store others: tables. That means what in other languages would be arrays (sequences) and dictionaries (maps) are the same thing.

This is probably the only thing that really bothers me in Lua. Sequential types are something fundamentally different from associative types in my mind, and I have on several occasions wanted them to be distinct.

## First order functions, closure and true tail calls

Not going to teach a CS class in a Quora answer to explain what the first two are, they are found in other languages but Lua does have them. The last one, however, is actually pretty rare in dynamic languages. Some Lisps have it, but not, for instance, Python, Ruby or Clojure.

What it means in practice is that returning a call to a function does not make the execution stack grow. For instance, this code will work for any value of n (ignoring numeric issues) whereas in other languages you would have a stack overflow for large values of n:

```lua
local function f(n)
  if n < 1 then
    return true
  else
    return f(n-1)
  end
end
```

