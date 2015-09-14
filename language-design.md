_Fill in each this file with your responses, placing each response after its
corresponding question._

---

**Question**

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

I never really considered the importance of operator overloading before, but Steele makes a very convincing argument for them:
opertor overloading allows an extension of a language (e.g., a class or package) to be as concise, familiar, and 'primitive'
as the underlying language. For example, in languages such as Java where operator overloading is not supported,
users must write an `add` function to represent the addition of two objects; the resulting code looks something like
`add(obj1, obj2)`, which gets the job done but isn't as simple and pleasing as the operator overloaded alternative `obj1 + obj2`.
C++ and Python are a couple languages that _do_ support operator overloading; and realizing that Python--
a language that I think people tend to not take very seriously for professional development--
supports a particularly preactical feature that Java does not, made me have a lot more respect for Python.
I had always thought of Python as more of a language for learners because (I hear) it has so much overhead
(which is maybe still significant), but its ease of use coupled with the ability to overload its unique,
natural language-feeling syntax is pretty awesome/powerful. My first thoughts went to the `in` operator,
but in all honesty, Java has done a great job of making iteration through a group of objects feel simpler.
In Java 5, the 'enhanced for loop' was added, which makes Java iteration feel very similar to iteration in Python
--though it's still missing a sort of natural language feeling.

<!--
* More respect for python because it supports operator overloading
* Operator overloading is possible in C++/Python but not in Java
* Operator overloading lets an extension of a language feel more familiar, convenient, and 'primitive:' like the language being extended.
* I never really considered the importance of operator overloading before, but I think it makes sense given the described benefits that users should be able to warp operators and keywords for personal use.
-->

> ...users will not wait for 'The Right Thing,' but will use what comes first and put up with the warts. *But*--users will not put up with the warts for all time. It is not long till they scream and moan and beg for changes. The small language will grow the warts will be shaved off or patched. [Steele, 1998]

We agree with Steele's idea that DSLs, or "small languages," (or really _any_ language) should be created,
at least to some extent, with flexibility in mind: languages tend to evolve, not only because the language designers decide to
update language features or philosophies, but also because the values and needs of the language's users change and adapt.
In the same vein, the adoption and continued use of a language can be perceived as a sort of function of the ability for users
to affect the direction and development of the language. Domain-specific needs change along with technology and society,
and the language will need to evolve and keep pace with the change,
or else risk fading to the background and being replaced by another language that--at least for the moment--
meets users' needs and expectations. When we came into this class, we had our own ideals about programming languages and DSLs,
in particular that a language if based on a particularly fruitful and foundational philosophy could be 'the right tool' for users;
but as with most things, designers and developers must continue to communicate with their users
and gauge the reception of their product in order to continue tuning the language to meet user expectations
whilst fixing the language within some philosophy or other boundary. This reading has been enlightening about
_how_ one should go about proposing, creating, and maintaining a DSL.

<!--
* Languages grow and develop, not only because of the language designers but also because of the users.
* The adoption of a language can be determined by the ability of its userbase to change the language to its needs
* I agree with the idea that DSLs or _small-languages_ should be created with flexibility in mind. Domain specific needs change as technology and people change, and the language will either have to keep up or be replaced.
* When I came into the class, I had ideals about programming languages and DSLs being able to be 'The Right Thing' but this reading has changed my mind about _how_ one should go about proposing and creating a DSL.
-->

> **Minimize mutability.** Immutable objects are simple, thread-safe, and freely sharable. [Bloch, 2006]

We initially hesitated to agree with this point, but with some debate and discussion between the two of us,
we realized the benefits and assented. While minimizing mutability might result in the language being
more verbose and less efficient (in terms of performance), users benefit by having an easier time reasoning about the state
of objects in the language, which helps to minimize the "conceptual weight," which Bloch also highlights as being important.
We recognize the importance of performance--after all, gross computation time can make a language virtually unusable--
but we believe the performance lost from making a language more verbose (at least in the case of minimizing mutability)
does not outweigh the gains in reducing conceptual weight, which in the long run can reduce time spent
debugging and reasoning about a program in the language. This quote captures another og Bloch's ideas about separating
APIs from their implementation details by creating a distinct layer between the inner working of the API and the programmer;
the less the programmer needs to be concerned with program state, the less the programmer needs to worry
about the underlying implementation.

<!--
* We initially hesitated to agree with this point, but with some debate we realized its benefits.
* With reduced mutability, users might end up being more verbose about what they want to accomplish, but it's more "simple," which helps to minimize the conceptual weight as well.
* We also likely lose some performance benefits, but the benefits gained likely outwieigh performance lost.
* this is hard to get in words :-(
* This quote captures the ideas from before about keeping APIs free of implementation details and creating a distinct layer between the inner workings of the API and the programmer. (Hoping to avoid the problem of leaky abstractions while providing a *useful and targeted* API.
-->

---

**Question**

How do the themes of _Growing a Language_ relate to the lab we did this week?

**Response**

The overarching theme we identified in _Growing a Language_ is that users should be able to extend programming languages. The keys to the theme are that programming languages should be user-oriented and user-defined. While the base of the programming language, in Bloch's words the _pattern_, of the programming language must be designed so that user programs and libraries are natural extensions of the base. The base that language designers provide should be just large enough for users to build and small enough for the program designers to be able to focus on their _pattern_. By enabling users to grow programming languages, they become contributers to the language. The size of the team working on the language is as large as the community and the people writing the language are the same as the ones who are using it. When we worked on the lab, we found ourselves asking how it would be easiest for us to use the language. That is, our design philosphy was that we, as programmers, are designing for like-minded programmers with the caveat that we hope others can use the library without reading into the basecode as much as we did. We want other users to be able to add to the library with the minimum amount of work, or conceptual weight. We redesigned the library so that the existing language would intuitive to build upon. We wanted to make it easy for users of the library to make changes to sound as easily, or intuitively as possible, but also be able to extend the language to include their own methods and objects with ease. The connection we made between growing the language and the redesign of the library is that we shared the goals of making additions to the library as _intuitive_ and _natural_. Users and programmers should be able to contribute and add upon what we build so that their contributions will become a natural extension of what we built. We think a large part of that has to do with the pattern that we establish with the methods that we wrote. We established a pattern that uses a sound object with methods that alter the sound object and separated what we felt were over-restrictive methods. In the newly designed class, users can do more specific actions to manipulate the sound. We hope that this control will enable them to write easier to understand code. We found the old code problematic since we could not easily discern the actions of the computer when calling methods. Future extensions of the class can easily follow the pattern that we developed to enable sound objects to transformed in other ways, and the extended class will seem like an updated version of the original.

<!--
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
-->

---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

##### A well-designed language:

* has a system or pattern for growth so that it can evolve with the needs of its users.
* stays true to a specific user, purpose, or philosophy so that development is directed and the language doesn't become obscure because it's trying to be too many things at once.
* requires just enough syntax to express an idea so that the syntax prescribed is concise and meaningful.
* "should be easy to use and hard to misuse:" [Bloch, 2006].
* allows users to expand the language in a way that feels like the underlying language (e.g., supports operator overloading).

##### Programs in a well-designed language:

* "[read] like prose" and are easy to understand--preferably, even by those who are not familiar with the language [Bloch, 2006].
* has components that can be altered in a predictable way to change the meaning of the program.
* behave in a predictable way and are obviously correct.

##### A poorly-designed language:

* employs trivial and unnecessary syntax.
* places a high conceptual burden on the user.
* requires reading lots of documentation to become familiar with the language.

##### Programs in a poorly-designed language:
* require excessive error handling.
* have to work around the limits of the language to accomplish anything of value.
* extend the language in an unnatural or distinct way.
* are neither obviously correct or incorrect.

---
 
**Question**

In what way is an API a language? 

**Response**

People use languages to express ideas. Programmers use programming languages to express ideas to a computer. Users program with APIs to express ideas to a system, which suggests that APIs _are_ a programming language. We define languages to have both vocabulary and grammar. This holds true for programming languages as well in the form of objects and methods forming vocabulary while syntax forms a grammar. APIs provide a vocabulary by a new set of methods or objects for the user to interact with the system. Some APIs have their own grammar, while other borrow grammar from the base programming language. Either way, the API has a grammar and vocabulary, just like a language, (sort-of, more on this later). We do not know the entire domain of APIs and are unsure if there are APIs that do not have a grammar, and would not be considered a language. We could not come up with an example of an API that provides either a grammar or vocabulary but not the other. However, we do assert that languages must have both in order to be understood. Some APIs are distinct from languages in that languages are able to communicate and express ideas without an outside grammar. That is, a language does not need to borrow a grammar from another language. In that way, where an API is reliant on the grammar of the underlying programming language and does not apply new grammar rules, APIs are not languages. APIs and languages also share design principles. The themes in _Growing a Language_ and _How to Design a Good API and Why It Matters_ coincide in the goals that the authors have in mind for APIs and languages. Languages and APIs should both be designed to make expressions of ideas easier. We believe that many of the language design philosphies we ran into in class can be applied to APIs to produce an effective and natural API. We have both run into APIs that are clunky and difficult to use and could use a language-oriented design approach.

<!--
* People use an API to express some idea (using the APIs syntax) to a system. Which suggests that it is a programming language.
* APIs and languages both have a vocabulary. Some APIs have grammars.
* APIs tend to grow and adapt to cater to their users.
* Some APIs are considered languages
* The design principles of APIs and programming languages are similar
* Languages and APIs are both designed to make expressions of ideas easier
-->

---

**Question**

The comments on the Pavlus article seem to set up a conflict between
professional programmers and everyone else. What is the essence of this
conflict? Do you sympathize more with the substance of the article's arguments
or with the substance of the majority of the commenters' arguments? Do you
sympathize more with the tenor of the article or the tenor of the majority of
the commenters?

**Response**

The conflict set up by the article and the comments is that professional programmers require robust tools with high specificity while everyone else may prefer languages that are higher-level abstractions. It seems that the premise of the article relies on the idea that most people should be able to understand code and that programming languages are not meeting their goals of being readable since people who do not program professionally cannot comprehend code. We disagree with this notion and side with the substance of the majority of the commenters' arguments. Programming should be something that is learned is not entirely intuitive to every English speaker. Just as English would not be intuitive to a Latin scholar, even though English is partially derived from Latin, programming languages are not intuitive to English speakers, even though many programs and languages are based in English. We believe that it is naive to think that programming languages can become intuitive to any English speaker, and that programming languages should be learned just like French and Spanish. Just like how there is overlapping grammar and vocabulary between Latin languages that ease fluency between speakers of those languages, we also believe this is how programmers quickly develop an ease of fluency between C derived languages. 

Some of the commenters argue that making programming tools more accessible only makes it easier for people to learn how to progrtam, but not necessarily how to program _well_, which is important. While we understand their concerns and agree to them to some extent, there should be some achievable balance through which someone who is familiar with a language can express that idea in the form of a program, and someone who is not familiar with that language, or programming altogether, can understand the intent of the program. Perhaps the most common programming languages do not quite achieve that lofty goal, but as one commenter points out "languages like C++, Perl, Python, and Java have stood the test of time because they provide the right balance between granular control over the computer and powerful abstraction" [Eric]. 

We also generally disagree with the article and the evidence brought up in the article since Perl is a difficult language to read in the first place. If they had compared a language that programmers typically start their programming experience such as Python, Processing, or Scratch, the results would be wildly different.

<!--
* There is an expectation to understand code because most code we see is written using English words.
* "languages like C++, Perl, Python, and Java have stood the test of time because they provide the right balance between granular control over the computer and powerful abstraction" [Eric, 2006]
* Some of the commenters argue that making programming tools more accessible only makes it easier for people to learn how to program, but not necessarily how to program _well_, which is important. While I understand their concerns and agree with them to some extent, there should be some achievable balance through which someone who is familiar with a language can express an idea in that language (via a program), and someone who is not familiar with that language (or programming altogether) can understand the intent of the program.
* ^^ This kind of goes back to the idea of a well-designed language being difficult to misuse or produce poorly written programs.
* Just as learning a new language is difficult, learning a programming language is difficult. The tools of a professional require domain knowledge and experience.
* High-level abstractions of code detract from the precision that programmers need to express their ideas. Otherwise, they would be limited by the scope of the abstraction.
* Perl is probably a poor example because it is regarded as a write-only language.
-->

---

**Question**

How do implementation choices (e.g., as an interpreter/compiler or as an
internal DSL) affect the user experience? Can or should we always hide our
implementation choices from users?

**Response**

Implementation choices change how user expressions are interpreted. Implementation choices can change how verbose or concise expressions in the language are. In this way, the feel of the language can be changed through the designer's choices. Good implementation choices give users intuitive results, a natural language feel, and an intuitive and sensible understanding of how the programming language realizes the user's ideas. We believe that good implementation choices will also lead to an interface that suggests what the implementation is to the user without the user needing to refer to documentation. (This is the notion that the language should read like documentation.) We do not believe that implementation choices should be hiden from the users. The documentation for a langauge should include implementation choices to enable users to make effective programing decisions. However, users should be able to comfortably program without detailed knowledege of the implementation. From our experiences, programming languages seem to imply their implementation details through their grammar, or syntax, so we do not believe that it is always possible to hide out implementation choices from users. Language designers should show the implementation choices so that users can use the language most effectively. Knowledgeable users can then provide feedback to the designer to help the language become the best that it can.

<!--
* Good implementation choices give users an intuitive result with a sensible understanding of how it accomplishes that task.
* Important implementation decisions should be inherent to the interface
..* the implementation should not be surprising given the interface
* Documentation should include implementation details in order to be effective and enable users to make effective programming decisions, but users should be able to comfortably program without knowing the implementation.
* Languages and their interfaces always imply implementation details, so we cannot always hide our implementation details. An ambiguous (and poor) interface would be able to hide implementation choices.
* We believe that we should not hide our implementation choices.
* Language designers should show the implementation choices so that users can use the language most effectively. Knowledgeable users can then provide feedback to the designer to help the language be the best that it can.
-->

---

**Question**

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

We believe that these two experiences of natural languages are not at odds with one another. Pavlus' statement that natural language replacements are more readable is correct. A simple example is the readability of for loops in Python and C++. When introducing for-loops to new programmers, the Python language is much more intuitive in expressing the actions of the program. We do recognize that _natural_ language as a programming language is extraordinarily difficult since natural language relies both on the context of speaker and the context of the listener. Trying to fit a natural language into the confines of a strict interpretation is the same issue that automated translators have. (As a fun aside, try to translate some phrases in Google Translate and then translate them back into English). Even the interpretation of simple phrases is not one-to-one and is often many-to-many, unideal for programming languages and their interpreters. We posit that natural language in a programming languages _is_ beneficial, but to an extent. We are unsure where the boundary lies between too much and too little but we will discuss this later. Historically, we find that programming languages generally neglect the clarity that natural language can provide.

In the design of a DSL, we would both elect to include natural language, to an extent. We could select a word that expresses an idea but avoid phrases or words that might express multiple ideas, at least to an audience similar to ourselves. We recognize that different contexts could make the natural language bits strange and unintuitive, but we believe the best way to avoid that is to stick to smaller phrases or words. (In our discussion, we chose to call these small phrases or words language elements.) Natural language is a tool avaiable to us to make a DSL more intuitive though a tool that we must be especially careful not to misuse. The danger of context driving a different interpreters of code is always present.

<!-- 
* We believe the two experiences are not at odds with one another. We believe Pavlus' statement that natural language replacements are more readable is correct. (Consider the readability of for loops in python and C++.) But we do think that full replacement is non-sensical and resembling a natural language is undesirable, as Cook mentions. 
* Including natural language in a programming language _is_ beneficial, but only to an extent.
* Historically, programming languages appear to neglect the clarity provided by including elements of natural language.

* We both would elect to include natural language in the design of a DSL, to an extent.
* Specifically, we would select a word that expresses an idea but avoid phrases or words that might express multiple ideas.
* Natural language is a tool that we can use to make a DSL more intuitive though one that we must be especially careful not to misuse. The danger of context driving a different interpretation of code is always present. 
-->

---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**

We read the articles separately. We sat next to each other and talked through each of the questions and simultaneously developed an outline for each of the questions. We split up the final write-up. However, we did an unfair initial split and adjusted for it as we did the write-up.

<!--
* We read the articles separately.
* We sat next to each other and talked through each of the questions and simultaneously developed an outline for each of the questions.
* We split up the final write-up (evens and odds).
-->

---
