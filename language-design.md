_Fill in each this file with your responses, placing each response after its
corresponding question._

---

**Question** Justis

Pick three quotes from the readings about language design. Good candidates 
are:

   + Something you agreed with / resonates with your own experience
   + Something you disagree with
   + Something that is interesting, a new idea or perspective you'd like to remember
   + Something you didn't understand

For each quote, describe what it was about the quote that led you pick it.

**Response**

> I have said in the past, and will say now, that I think it would be a good thing
> for the Java programming language to ... let the user define overloaded operators.
> Just as a user can code methods that can be used in just the same way as
> methods that are built in, the user ought to have a way to define operators for user
> defined classes that can be used in just the same way as operators that are built in. [Steele, 1998]

* More respect for python because it supports operator overloading
* Operator overloading is possible in C++/Python but not in Java
* Operator overloading lets an extension of a language feel more familiar, convenient, and 'primitive:' like the language being extended.
* I never really considered the importance of operator overloading before, but I think it makes sense given the described benefits that users should be able to warp operators and keywords for personal use.


> ...users will not wait for 'The Right Thing,' but will use what comes first and put up with the warts. *But*--users will not put up with the warts for all time. It is not long till they scream and moan and beg for changes. The small language will grow the warts will be shaved off or patched. [Steele, 1998]

* Languages grow and develop, not only because of the language designers but also because of the users.
* The adoption of a language can be determined by the ability of its userbase to change the language to its needs
* I agree with the idea that DSLs or _small-languages_ should be created with flexibility in mind. Domain specific needs change as technology and people change, and the language will either have to keep up or be replaced.
* When I came into the class, I had ideals about programming languages and DSLs being able to be 'The Right Thing' but this reading has changed my mind about _how_ one should go about proposing and creating a DSL.


> **Minimize mutability.** Immutable objects are simple, thread-safe, and freely sharable. [Bloch, 2006]

* We initially hesitated to agree with this point, but with some debate we realized its benefits.
* With reduced mutability, users might end up being more verbose about what they want to accomplish, but it's more "simple," which helps to minimize the conceptual weight as well.
* We also likely lose some performance benefits, but the benefits gained likely outwieigh performance lost.
* this is hard to get in words :-(
* This quote captures the ideas from before about keeping APIs free of implementation details and creating a distinct layer between the inner workings of the API and the programmer. (Hoping to avoid the problem of leaky abstractions while providing a *useful and targeted* API.

---

**Question** Kevin

How do the themes of _Growing a Language_ relate to the lab we did this week?

**Response**

_Growing a Language_ Themes:
* When users want to extend the language, the extension should _feel_ like a part of the language rather than a distinct entity.
* Language should change and grow and languages that cannot naturally grow will wither away.
* Users should be able to contribute to the growth of a language.
* Provide just enough tools for the user be able to everything they need to, but no more than that.

Lab Themes:
* Design to make it easier and more natural for its users to accomplish specific tasks.
* Make it easy for users to make as many changes to the sound as they want with the minimum amount work or thought.
* Design to make it easy for users to add more methods in the future.

Connections:
* An _easy_ way to add methods should also be _intuitive_ and _natural_ in the language or library that we build. This also connects to the idea that users should be able to contribute, and to encourage users to contribute to the language by making their contributions a part of the language.

---

**Question** Justis

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

#### A well-designed language:

* has a system or pattern for growth.
* has a purpose or specific user in mind
* sticks to a consistent philosophy.
* "should be easy to use and hard to misuse" [Bloch, 2006]
* enables users to expand the language in a way that feels like the original language.

#### Programs in a well-designed language:

* are easy to understand, "reads like prose" [Bloch, 2006]
* can be altered in a predictable way
* behave in a predictable way

#### A poorly-designed language:

* employs trivial and unnecessary syntax
* is inconsistent in its philosophy
* requires reading lots of documentation to become familiar with the language

#### Programs in a poorly-designed language:
* require excessive exception handling
* have to work around the limits of the language
* extend the language in an unnatural or distinct way
* are not obviously 'correct' (or incorrect)

---
 
**Question** Kevin

In what way is an API a language? 

**Response**

* People use an API to express some idea (using the APIs syntax) to a system. Which suggests that it is a programming language.
* APIs and languages both have a vocabulary. Some APIs have grammars.
* APIs tend to grow and adapt to cater to their users.
* Some APIs are considered langauges
* The design principles of APIs and langauges are similar
* Languages and APIs are both designed to make expressions of ideas easier

---

**Question** Justis

The comments on the Pavlus article seem to set up a conflict between
professional programmers and everyone else. What is the essence of this
conflict? Do you sympathize more with the substance of the article's arguments
or with the substance of the majority of the commenters' arguments? Do you
sympathize more with the tenor of the article or the tenor of the majority of
the commenters?

**Response**

* There is an expectation to understand code because most code we see is written using English words.
* "languages like C++, Perl, Python, and Java have stood the test of time because they provide the right balance between granular control over the computer and powerful abstraction" [Eric, 2006]
* Some of the commenters argue that making programming tools more accessible only makes it easier for people to learn how to program, but not necessarily how to program _well_, which is important. While I understand their concerns and agree with them to some extent, there should be some achievable balance through which someone who is familiar with a language can express an idea in that language (via a program), and someone who is not familiar with that language (or programming altogether) can understand the intent of the program.
* ^^ This kind of goes back to the idea of a well-designed language being difficult to misuse or produce poorly written programs.
* Just as learning a new language is difficult, learning a programming language is difficult. The tools of a professional require domain knowledge and experience.
* High-level abstractions of code detract from the precision that programmers need to express their ideas. Otherwise, they would be limited by the scope of the abstraction.
* Perl is probably a poor example because it is regarded as a write-only language.

---

**Question** Kevin

How do implementation choices (e.g., as an interpreter/compiler or as an
internal DSL) affect the user experience? Can or should we always hide our
implementation choices from users?

**Response**

* Good implementation choices give users an intuitive result with a sensible understanding of how it accomplishes that task.
* Important implementation decisions should be inherent to the interface
..* the implementation should not be surprising given the interface
* Documentation should include implementation details in order to be effective and enable users to make effective programming decisions, but users should be able to comfortably program without knowing the implementation.
* Languages and their interfaces always imply implementation details, so we cannot always hide our implementation details. An ambiguous (and poor) interface would be able to hide implementation choices.
* We believe that we should not hide our implementation choices.
* Language designers should show the implementation choices so that users can use the langauge most effectively. Knowledgeable users can then provide feedback to the designer to help the language be the best that it can.

---

**Question** Justis

The Pavlus article mentions the researchers' comments that people preferred
"natural-language replacements for some of the more abstruse syntax". In other 
words, people found it easier to work with code that looks more like a human language (e.g.,
English). Consider the following quote by William R. Cook, one of the creators
of JavaScript:


> The experiment in designing a language that resembled natural languages (English
> and Japanese) was not successful. It was assumed that scripts should be
> presented in “natural language” so that average people could read and write
> them. … In the end the syntactic variations and flexibility did more to confuse
> programmers than to help them out. It is not clear whether it is easier for
> novice users to work with a scripting language that resembles natural language,
> with all its special cases and idiosyncrasies. The main problem is that
> AppleScript only appears to be a natural language: in fact, it is an artificial
> language, like any other programming language. … even small changes to the
> script may introduce subtle syntactic errors that baffle users. It is easy to
> read AppleScript, but quite hard to write it.
[[Cook 2007, page 1-20]](https://dl.acm.org/citation.cfm?doid=1238844.1238845)

Are these two experiences of natural languages at odds with one another? Would
you choose to include natural language in the design of a DSL? If so, how might
you do so? If not, why not?

**Response**

* We believe the two experiences are not at odds with one another. We believe Pavlus' statement that natural language replacements are more readable is correct. (Consider the readability of for loops in python and C++.) But we do think that full replacement is non-sensical and resembling a natural language is undesirable, as Cook mentions. 
* Including natural language in a programming language _is_ beneficial, but only to an extent.
* Historically, programming languages appear to neglect the clarity provided by including elements of natural language.

* We both would elect to include natural language in the design of a DSL, to an extent.
* Specifically, we would select a word that expresses an idea but avoid phrases or words that might express multiple ideas.
* Natural language is a tool that we can use to make a DSL more intuitive though one that we must be especially careful not to misuse. The danger of context driving a different interpretation of code is always present. 

---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**

We read the articles separately.
We sat next to each other and talked through each of the questions and simultaneously developed an outline for each of the questions.
We split up the final write-up (evens and odds).

---
