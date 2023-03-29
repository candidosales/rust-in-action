# rust-in-action

## Chapter 1

- “We can eliminate these by compiling a release build using cargo’s --release flag.”
- “It’s possible to further reduce the output by adding the -q flag to cargo commands. -q is shorthand for quiet. The following snippet shows what that looks like:”

```bash
$ cargo run -q --release
```

1.6.1 Goal of Rust: Safety

Rust programs are free from

- Dangling pointers—Live references to data that has become invalid over the course of the program (see listing 1.3)
- Data races—The inability to determine how a program will behave from run to run because external factors change (see listing 1.4)
- Buffer overflow—An attempt to access the 12th element of an array with only 6 elements (see listing 1.5)
- Iterator invalidation—An issue caused by something that is iterated over after being altered midway through (see listing 1.6)

“After some thought, it becomes apparent why the if test receives the wrong type. The if is not receiving an integer. It’s receiving the result of an assignment. In Rust, this is the blank type: (). () is pronounced unit.14”

“1.8 Downsides of Rust”

“1.8.1 Cyclic data structures

In Rust, it is difficult to model cyclic data like an arbitrary graph structure. Implementing a doubly-linked list is an undergraduate-level computer science problem. Yet Rust’s safety checks do hamper progress here. If you’re new to the language, avoid implementing these sorts of data structures until you’re more familiar with Rust.”

“1.8.2 Compile times

Rust is slower at compiling code than its peer languages. It has a complex compiler toolchain that receives multiple intermediate representations and sends lots of code to the LLVM compiler.”

“1.9 TLS security case studies”

“Rust does not protect you from logical errors. It ensures that your data is never able to be written in two places at the same time. It does not ensure that your program is free from all security issues.”

1.10 Where does Rust fit best?

- 1.10.1 Command-line utilities
- 1.10.2 Data processing
- 1.10.3 Extending applications
- 1.10.4 Resource-constrained environments
- 1.10.5 Server-side applications
- 1.10.6 Desktop applications
- 1.10.7 Desktop
- 1.10.8 Mobile
- 1.10.9 Web
- 1.10.10 Systems programming

  1.12 Rust phrase book

- Empowering everyone—All programmers regardless of ability or background are welcome to participate. Programming, and particularly systems programming, should not be restricted to a blessed few.
- Blazingly fast—Rust is a fast programming language. You’ll be able to write programs that match or exceed the performance of its peer languages, but you will have more safety guarantees.
- Fearless concurrency—Concurrent and parallel programming have always been seen as difficult. Rust frees you from whole classes of errors that have plagued its peer languages.
- No Rust 2.0—Rust code written today will always compile with a future Rust compiler. Rust is intended to be a reliable programming language that can be depended upon for decades to come. In accordance with semantic versioning, Rust is never backward-incompatible, so it will never release a new major version.
- Zero-cost abstractions—The features you gain from Rust impose no runtime cost. When you program in Rust, safety does not sacrifice speed.
