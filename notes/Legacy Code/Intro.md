
Retrofitting tests onto existing code is a tough problem and an important skill. It’s high time we tackled it.

# The Challenge
There’s a chicken-and-egg problem with adding tests to existing code. The majority of your tests should be fine-grained unit tests; they run faster and are less likely to break than other forms of tests. Unfortunately, these sorts of tests need to poke into your codebase in order to set up dependencies and validate state. Unless your code was written with testability in mind (it wasn’t!), you can’t test it.

So you need to refactor. The problem is that, in a complex codebase, refactoring is dangerous. Side effects lurk behind every function. Twists of logic wait to trip you up. In short, if you refactor, you’re likely to break something without realizing it.
So you need tests. But to test, you need to refactor. But to refactor, you need tests. Etc., etc., argh.

# The Solution
To break the chicken-and-egg dilemma, we need some way of refactoring without breaking code. One option is to just run manual tests after every change, but that is slow and error-prone.

What we need is the simplicity of manual tests and the speed and convenience of automated tests. In other words, pinning tests.

A “pinning test” is not a good test. It doesn’t try to be. It’s just the simplest, fastest-running test you can write that will allow you to refactor your code. It’s often an end-to-end test, but it could also look at your log files, monkey-patch a core library function, or do something similarly ridiculous.

The key here is that the pinning test lets you do your dozens of tiny refactorings loop really quickly. As the code improves, you add high-quality unit tests. Once the tests are good enough, you get rid of the pinning test. Lather, rinse, repeat.

# The Strategy
Overall, the key is to think small. Don’t try to fix everything all at once. Choose something small, preferably something you needed to work on anyway, and fix that. Then fix the next thing, and the next thing. If you keep fixing the areas you’re actually working in, then the parts of the system you touch most will improve most quickly.

1. Reverse Engineer Design : Reflective Design 
2. Decide Goal
3. Determine Test Strategy 
4. Set Up Automation 
5. Create Pinning Tests
6. Refactor and Add Unit Tests

Ref: 
- http://www.letscodejavascript.com/v3/blog/2014/02/the\_legacy\_code\_challenge
- http://wiki.c2.com/?PinningTests


