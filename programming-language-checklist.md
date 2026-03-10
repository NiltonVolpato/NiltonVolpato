# Programming Language Checklist

## New and Updated Version!

*Includes some of the modern language design discourse.* 
*Nilton Volpato and Claude (Anthropic), 2026*

*Original by Colin McMillen, Jason Reed, and Elly Fong-Jones, 2011-10-10.*

---

You appear to be advocating a new programming language. Your language will not work. Here is why it will not work.

To begin, please classify your language:

### Paradigm
- [ ] functional
- [ ] imperative
- [ ] object-oriented
- [ ] procedural
- [ ] stack-based
- [ ] concatenative
- [ ] actor-based
- [ ] reactive / dataflow
- [ ] logic / constraint-based
- [ ] probabilistic
- [ ] "multi-paradigm"
- [ ] visual
- [ ] quantum

### Evaluation strategy
- [ ] eager
- [ ] lazy
- [ ] mixed (good luck specifying that)

### Type discipline
- [ ] statically typed
- [ ] dynamically typed
- [ ] gradually typed
- [ ] pure
- [ ] impure
- [ ] non-hygienic macros

### Execution model
- [ ] compiled (ahead-of-time)
- [ ] interpreted
- [ ] JIT compiled
- [ ] transpiled to: _______________________
- [ ] runs on a custom VM
- [ ] runs on the JVM
- [ ] runs in the browser (WASM)
- [ ] runs on the GPU
  - [ ] CUDA
  - [ ] Vulkan compute
  - [ ] Metal
  - [ ] vendor-agnostic (how?)

### Turing-completeness
- [ ] Turing-complete
- [ ] Turing-incomplete by design
  - [ ] guaranteed termination
  - [ ] no general recursion
  - [ ] no unbounded loops
  - [ ] embeddable / sandboxed
  - [ ] total functional
- [ ] Turing-incomplete by accident

### Target audience
- [ ] general purpose
- [ ] domain-specific: _______________________
- [ ] systems programming
- [ ] scripting
- [ ] configuration / data description
- [ ] beginner-friendly
- [ ] non-programmer-friendly
- [ ] completely incomprehensible

---

## You appear to believe that:

### Hardware and runtime
- [ ] Syntax is what makes programming difficult
- [ ] Garbage collection is free
- [ ] Tracing GC and reference counting are equivalent
- [ ] Computers have infinite memory
- [ ] Multicore CPUs are a temporary inconvenience
- [ ] Specifying behaviors as "undefined" means programmers won't rely on them
- [ ] "Spooky action at a distance" makes programming more fun

### Memory safety
- [ ] Borrow checking is too hard, but your solution isn't
- [ ] Ownership and borrowing, but simpler
- [ ] Memory safety can be achieved with sufficiently strongly worded documentation

### Adoption and ecosystem
- [ ] Nobody really needs:
  - [ ] concurrency
  - [ ] async I/O
  - [ ] a REPL
  - [ ] debugger support
  - [ ] a language server (LSP)
  - [ ] IDE support
  - [ ] a package manager
  - [ ] a package registry
  - [ ] syntax highlighting in any editor
  - [ ] to interact with code not written in your language
- [ ] The entire world speaks 7-bit ASCII
- [ ] Unicode is someone else's problem
- [ ] Scaling up to large software projects will be easy
- [ ] Convincing programmers to adopt a new language will be easy
- [ ] Rewriting existing codebases will be easy
- [ ] Programmers love writing lots of boilerplate
- [ ] Programmers love *not* writing boilerplate because your macro system handles it
- [ ] WebAssembly makes portability a solved problem

### LLMs and AI
- [ ] LLMs will just generate all the code anyway, so language ergonomics don't matter
- [ ] LLMs will never be able to write your language, which is somehow a selling point
- [ ] Your language will be popular enough that LLMs will eventually learn it
  - [ ] despite it not yet being popular enough for LLMs to learn it
  - [ ] despite LLMs not knowing it being one of the reasons it won't become popular
- [ ] Putting a `llms.txt` on your website solves the LLM training problem
  - [ ] Your language is so complex that after reading `llms.txt` there is no context window left for actual work

### Type system ambitions
- [ ] Your effect system will replace monads and everyone will be fine with that
- [ ] Your type system is so powerful that no program with a runtime error can be expressed
  - [ ] no program can be expressed

---

## Unfortunately, your language has/lacks:

### Syntax and structure
- [ ] comprehensible syntax
- [ ] semicolons
- [ ] significant whitespace
- [ ] significant indentation *and* significant braces (somehow)
- [ ] macros
- [ ] no macros
- [ ] hygienic macros
- [ ] a macro system that is itself a full programming language
- [ ] infix operators
- [ ] user-defined operators
- [ ] Unicode operators
- [ ] nested comments
- [ ] multi-line strings
- [ ] string interpolation
- [ ] regexes

### Syntax minutiae
- [ ] It is modern language consensus that trailing commas are the correct choice, however:
  - [ ] your grammar does not accept trailing commas
  - [ ] your formatter puts commas at the beginning of the line
  - [ ] your lists have no commas at all, making them extremely ambiguous
  - [ ] your grammar requires trailing commas, breaking everyone's muscle memory in the other direction
- [ ] Your string escaping rules are:
  - [ ] identical to C, which was already wrong in 1972
  - [ ] novel, underdocumented, and subtly wrong
  - [ ] whatever the host language does, which you didn't check
- [ ] Integer overflow:
  - [ ] wraps silently
  - [ ] panics in debug, wraps in release
  - [ ] is undefined behavior (welcome back)
  - [ ] is a type error (you have thought about this too hard)

### Type system
- [ ] implicit type conversion
- [ ] explicit casting
- [ ] type inference
- [ ] local type inference
- [ ] global type inference (good luck)
- [ ] algebraic datatypes
- [ ] recursive types
- [ ] polymorphic types
- [ ] higher-kinded types
- [ ] dependent types
- [ ] linear / affine types
- [ ] ownership and borrowing
- [ ] an effect system
- [ ] row polymorphism
- [ ] union types
- [ ] intersection types
- [ ] gradual typing
- [ ] covariant array typing
- [ ] monads
- [ ] subtyping
- [ ] multiple inheritance
- [ ] operator overloading

### Control flow
- [ ] goto
- [ ] exceptions
- [ ] result/error types
- [ ] closures
- [ ] tail recursion
- [ ] tail call optimization (guaranteed)
- [ ] coroutines
- [ ] async/await
- [ ] green threads
- [ ] algebraic effects
- [ ] call/cc
- [ ] call-by-value
- [ ] call-by-name
- [ ] call-by-reference
- [ ] pattern matching
- [ ] exhaustive pattern matching

### Tooling
- [ ] a package manager
- [ ] a package registry (online)
- [ ] support for multiple versions of the same package in one project
  - [ ] which causes binary bloat
  - [ ] which causes diamond dependency nightmares
- [ ] only one version of each package allowed per project
  - [ ] which causes dependency hell
  - [ ] which makes you reinvent virtualenv
- [ ] a build system
- [ ] a formatter
- [ ] a linter
- [ ] a language server (LSP)
- [ ] a debugger
- [ ] a tree-sitter grammar
- [ ] syntax highlighting in any editor:
  - [ ] VS Code
  - [ ] Zed
  - [ ] Neovim
  - [ ] Emacs
  - [ ] Vim (not Neovim)
  - [ ] any editor released after 2010
- [ ] an IDE extension
- [ ] go-to-definition
- [ ] find-all-references
- [ ] inline type hints
- [ ] autocompletion that works

### Runtime and interop
- [ ] reflection
- [ ] a foreign function interface
- [ ] a C FFI
- [ ] a WASM compilation target
- [ ] a WASM *runtime*
- [ ] a JVM target
- [ ] a JavaScript target
- [ ] a GPU target

---

## The following philosophical objections apply:

### Approachability
- [ ] Programmers should not need to understand category theory to write "Hello, World!"
- [ ] Programmers should not need to understand linear logic to use your standard library
- [ ] Programmers should not develop RSI from writing "Hello, World!"
- [ ] Programmers should not need to read your dissertation to understand the type errors
- [ ] The most significant program written in your language is:
  - [ ] its own compiler
  - [ ] not even its own compiler
  - [ ] a Fibonacci calculator
  - [ ] a "Hello, World!" that took 4 hours to get past the type checker

### Specification and correctness
- [ ] No language spec
- [ ] "The implementation is the spec"
  - [ ] The implementation is closed-source
  - [ ] covered by patents
  - [ ] not owned by you
  - [ ] written in a language most contributors don't know
- [ ] Your type system is:
  - [ ] unsound
  - [ ] sound but useless in practice
  - [ ] so expressive that "Hello, World!" does not type-check
  - [ ] so expressive that nothing type-checks
- [ ] Your language cannot be unambiguously parsed
  - [ ] a proof of same is attached
  - [ ] invoking this proof crashes the compiler

### Naming
- [ ] The name of your language is:
  - [ ] impossible to find on Google
  - [ ] already a very common English word
  - [ ] an acronym that expands to a recursive joke
  - [ ] a curse word in at least three languages
  - [ ] impossible to pronounce
  - [ ] going to be mispronounced by everyone, including you in interviews

### Grand claims
- [ ] Interpreted languages will never be as fast as C
- [ ] Compiled languages will never be "extensible"
- [ ] Writing a compiler that understands English is AI-complete
- [ ] Your language relies on an optimization which has never been shown possible
- [ ] There are fewer than 100 programmers on Earth:
  - [ ] smart enough to use your language
  - [ ] patient enough to use your language
  - [ ] who have heard of your language
- [ ] __________________________ takes exponential time
- [ ] __________________________ is known to be undecidable
- [ ] __________________________ requires solving the halting problem

---

## Your implementation has the following flaws:

### Fundamental misunderstandings
- [ ] CPUs do not work that way
- [ ] RAM does not work that way
- [ ] VMs do not work that way
- [ ] Compilers do not work that way
- [ ] Compilers cannot work that way
- [ ] You don't seem to understand:
  - [ ] basic optimization techniques
  - [ ] basic systems programming
  - [ ] pointers
  - [ ] functions
  - [ ] what "zero-cost abstraction" means
  - [ ] that "blazing fast" requires a benchmark

### Compiler behavior
- [ ] Shift-reduce conflicts in parsing seem to be resolved using `rand()`
- [ ] You require the compiler to be present at runtime
- [ ] You require the language runtime to be present at compile-time
- [ ] Your compiler is written in Haskell and takes 45 minutes to build from source
- [ ] Your compiler errors are:
  - [ ] completely inscrutable
  - [ ] inscrutable and link to a GitHub issue marked "wontfix"
  - [ ] inscrutable and reference a paper behind a paywall
  - [ ] actually pretty good, which just makes the unsolvable type errors more infuriating
- [ ] Dangerous behavior is only a warning
- [ ] Safe behavior is somehow also a warning
- [ ] The compiler crashes if you look at it funny
- [ ] The VM crashes if you look at it funny
- [ ] Compilation requires more RAM than the program will ever use at runtime
- [ ] Incremental compilation is "planned"

### Tooling flaws
- [ ] The language server:
  - [ ] does not exist
  - [ ] crashes VS Code
  - [ ] crashes Zed
  - [ ] crashes the editor and takes the unsaved file with it
  - [ ] works, but only for files under 200 lines
- [ ] Your package manager:
  - [ ] downloads half of npm
  - [ ] *is* npm
  - [ ] does not exist yet
  - [ ] exists but has no packages
  - [ ] has packages but they are all written by you

---

## Additionally, your marketing has the following problems:

### Claims
- [ ] Unsupported claims of increased productivity
- [ ] Unsupported claims of greater "ease of use"
- [ ] Unsupported claims of memory safety
- [ ] Your elevator pitch is:
  - [ ] "It's like Rust, but without the borrow checker" (it leaks memory)
  - [ ] "It's like Python, but fast" (it isn't)
  - [ ] "It's like Haskell, but practical" (it isn't)
  - [ ] "It's like Go, but with more features" (Go programmers do not want more features)
  - [ ] "It's AI-native" (undefined)
  - [ ] "It's safe *and* fast *and* easy" (pick one)

### Benchmarks
- [ ] Obviously rigged benchmarks:
  - [ ] Graphics, simulation, or crypto benchmarks where your code just calls handwritten assembly through your FFI
  - [ ] String-processing benchmarks where you just call PCRE
  - [ ] Matrix-math benchmarks where you just call BLAS
  - [ ] Your benchmark program does not actually compute the correct answer
- [ ] Nobody really believes that your language is faster than:
  - [ ] assembly
  - [ ] C
  - [ ] FORTRAN
  - [ ] Java
  - [ ] Ruby
  - [ ] Prolog
  - [ ] the language you claim to replace

### Community and documentation
- [ ] Your README has more badges than lines of documentation
- [ ] Your documentation consists entirely of a single blog post
- [ ] Your "community" is a Discord server with 12 members, 11 of whom are you
- [ ] You gave a talk at a local meetup and called it "production-ready"

### Rejection of established knowledge
- [ ] Rejection of orthodox programming-language theory without justification
- [ ] Rejection of orthodox systems programming without justification
- [ ] Rejection of orthodox algorithmic theory without justification
- [ ] Rejection of basic computer science without justification

---

## Taking the wider ecosystem into account, I would like to note that:

- [ ] Your complex sample code would be one line in: _______________________
- [ ] We already have:
  - [ ] an unsafe imperative language
  - [ ] a safe imperative OO language
  - [ ] a safe statically-typed eager functional language
  - [ ] a language with an ownership system
  - [ ] a gradually typed scripting language
  - [ ] seventeen gradually typed JavaScript supersets
- [ ] You have reinvented:
  - [ ] Lisp but worse
  - [ ] Scheme but worse
  - [ ] ML but worse
  - [ ] Haskell but without the academic credibility
  - [ ] Rust but without the safety guarantees
  - [ ] Go but with fewer deliberate limitations
  - [ ] JavaScript but worse
  - [ ] TypeScript but worse
  - [ ] Java but worse
  - [ ] C++ but worse
  - [ ] PHP but worse
  - [ ] PHP better, but that's still no justification
  - [ ] Brainfuck but non-ironically
  - [ ] Prolog but without the logic
  - [ ] Erlang but for people who haven't heard of Erlang
  - [ ] APL but with even more Unicode
  - [ ] COBOL but for the cloud
- [ ] Your language is a worse Python with a Rust syntax
- [ ] Your language is a worse Rust with a Python syntax
- [ ] Your language is Python, but also compiled, JIT, SIMD, GPU, and still figuring out what it is
- [ ] An LLM generated the initial spec and you edited it slightly
- [ ] An LLM generated the initial spec and you did not edit it

---

## In conclusion, this is what I think of you:

- [ ] You have some interesting ideas, but this won't fly.
- [ ] This is a bad language, and you should feel bad for inventing it.
- [ ] Programming in this language is an adequate punishment for inventing it.
- [ ] You have inadvertently reinvented a language from the 1970s. Please read a book.
- [ ] Impressive. You have made something worse than COBOL while trying to improve on Python.
- [ ] Your language cannot be used by humans, LLMs, or future civilizations that find your GitHub repo.
