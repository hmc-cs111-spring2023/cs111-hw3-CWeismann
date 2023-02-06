# Free project 2

## The user and a language

This section describes who the project would serve and why a language might be a
good way to meet their needs.

### What's the need?

_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

Accordion music is generally written on a regular grand staff, with keyboard notes written in the treble clef and bass notes/Stradella chords written in the bass clef. However, a great deal is left out in these directions, like when to reverse bellows direction, or sort of tacked on top, like the notation for which chord to play, when to switch registers, bellows shake, and noise-sounds.

Additionally, one of the virtues of having the Stradella bass system, in which chords can be played with a single button, is that beginner accordionists do not have to learn how chords are constructed, and more information could be communicated quicker with a more compact notation, which could serve as a sort of tablature (tab) or fake book for players.

### Why a language?

_Why is a DSL appropriate for your user(s)? How does it address the need?_

It provides a compact, easy-to-learn notation, that could also easily be converted into a MIDI file to allow playback to help learn new songs. This will address some of the difficulty of learning music for new accordionists, and standardize some of the strange notation that is used currently.

### Why you?

_What excites you about this idea? How did you come up with it?_

I'm an amateur accordionist, and while I already know how to read music, I know its a barrier of entry for many others, which especially irks me for such a beginner-friendly instrument. A quite skilled accordionist that I sometimes watch lesson videos of noted that he was unable to read music, which got me thinking about how accordion notation could be improved.

### Domain

_Describe the project's domain in five words._

Beginner-friendly notation for accordions

### Interface (syntax)

_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

The user interacts with the language by reading and/or writing the notation to a file, which can then be compiled into a more visual-friendly notation, or played out as a MIDI file. This allows the DSL to interact with both parts of the domain of music notation: its visual form and its audible form.

### Operation (semantics)

_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

"Running" a program in this DSL will be more like running an HTML/CSS or Markdown file: it will mostly just render a file in a specific notation.

### Expressiveness

_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to write notation for basically any traditional (not free-bass) accordion piece. It should be doable, but more difficult, to write free-bass notation (since that niche is pretty much served by regular notation already). It should be very difficult to write anything involving microtonality or other music effects that cannot be performed on an unmodified accordion.

### Related work

_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

Not really, although there is this document, which attempts to standardize regular notation for accordions.
https://erikhojsgaard.dk/Resources/Handbook.pdf

My guess for why there isn't an existing DSL is lack of demand: accordions have seen a steep drop in popularity (at least in the United States) since the 1960s, and most players are old-timers who aren't bothered by having to read music. I think having a simple notation, like guitar tab or piano fake books, might make it easier for newcomers, especially younger people, to get into playing accordion.

## The Project

This section examines whether the idea makes for a good CS 111 project.

### Suitability

_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

This language would likely have quite a bit more systems programming, mostly to render the actual appearance of the notation, but I think there will still be a significant amount of language work. My guess would be about 50-50, with the language aspects frontloaded and the systems aspects at the end of the project.

### Scope

_How big an idea is this? How ambitious is this project?_

This is a fairly big project, but well within the scope of the class. Converting the notation to MIDI is probably a bit more than we have time for, but it would be a cool followup nonetheless.

### Benefits and drawbacks

_Why might this be a good idea for a project? Why might this not be a good idea
project?_

Benefits:
- Interdisciplinary
- Could be generalized to more instruments as a followup project

Drawbacks:
- Standard music notation already exists
- Compiles into something static; might not be as exciting as other projects
