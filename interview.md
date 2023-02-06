# Interview project

## The user and a language

This section describes who the project would serve and why a language might be a
good way to meet their needs.

### What's the need?

_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

Precision machining often requires referencing copious amounts of printed tables to ensure perfect accuracy. However, this can take a significant amount of time, only made worse by imperial-metric conversions and tool quirks.

### Why a language?

_Why is a DSL appropriate for your user(s)? How does it address the need?_

While merely performing table lookups would be better suited to somethink like a database with lookups, the ability for individual machinists to customize the lookups to their own shop and relevant specifications means that a DSL is more flexible and more useful.

### Why you?

_What excites you about this idea? How did you come up with it?_

I interviewed one of the assistant heads of the machine shop, and she said that it would significantly improve the lives of many machinists, as it makes a tedious step much faster.

### Domain

_Describe the project's domain in five words._

Customizable reference tables for machining

### Interface (syntax)

_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

The user would be able to type into a terminal prompt in a sort of SQL-like access, e.g. FIND tap WHERE thread=70% AND drill=50, to which the program would then spit out "2-64". The user can also add special operations in a file, like something that would tell you where a specific item was stored in the shop, or some sort of situation-relevant information.

### Operation (semantics)

_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When a program runs it will load all of the information into some sort of accessible database, then prompt the user to query that database. The only errors I can think of occurring are a malformed query, which can just be rejected by the language and notify the user in the shell, or a mistake in a file which will ideally be caught at database load-time and either fail the load or load without the mistake.

### Expressiveness

_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to access any information that could normally be communicated in a paper chart. It should be possible to make mathematical conversions and other useful tools, but probably not as a "main" language feature. It should be impossible to edit the database from within the prompt, to stop malicious tampering.

### Related work

_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I wasn't able to find any on the internet, although it's possible that you could consider an existing body of tables, like Machinery's Handbook, 31st Edition, to be a sort of analog DSL in this field. If we consider that to be the existing DSL, I would guess that most machinists have spent their entire career using that (and memorizing especially relevant information), so they don't feel the need for a DSL as keenly as newer machinists.

## The Project

This section examines whether the idea makes for a good CS 111 project.

### Suitability

_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

To make a usable version of this, I would anticipate that the vast majority (>80%) of the work would be systems aspects, unfortunately.

### Scope

_How big an idea is this? How ambitious is this project?_

I don't think the project is terribly ambitious or huge, but there is just a ton of groundwork to do to make it useful.

### Benefits and drawbacks

_Why might this be a good idea for a project? Why might this not be a good idea
project?_

Benefits:
- Large group of interested people
- The machine shop could use it

Drawbacks:
- So much data entry
- Probably very boring for most people
