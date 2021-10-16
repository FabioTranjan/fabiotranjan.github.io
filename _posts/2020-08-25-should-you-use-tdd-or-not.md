---
layout: post
author: ftranjan
---
One of the biggest flame wars in the tech industry is: should I test first or test after code? Some people will advocate in favor of the TDD (_test-driven development_) technique. Others prefer to focus on the logic first and then test to assert the expected behavior.

---

Before even thinking about TDD, we need to know why to test in the first place. Some of the benefits of automated testing are:
1. Protect your current behavior from breaking against _regressions_, be confident that your code continues to work is key.
2. Good tests allow you to _refactor_ the logic with confidence, as a consequence, the code quality increase, and fewer bugs happen.
3. A test serves as a _concrete_ contract, acting as a _client_, and determining the expected behavior and design of your system.

TDD or _test-driven development_ is based on a technique first appeared on _eXtreme Programming_ as a test-first approach and after advocate by Kent Beck in his excellent book _Test Driven Development: By Example_. Most of the developers already heard about it, but a lot of them don’t know *HOW*, *WHY*, and *WHEN* to use it in the first place.

### Why TDD?

Let’s say you are a developer and need to develop a new critical feature, such as a new currency abstraction that allows you to execute operations (sum, subtraction, etc.) on different currencies (10$ + 5€ = ?). Your boss is waiting for a response, is that possible or not? Then you start coding and after some time nothing happens, you’re just stuck on how to start all these complex and abstract ideas. You are under pressure and need to develop this fast.

Then you discover a technique called TDD, it advocates that you don't know to code all the logic from start, but you can build your feature step-by-step, testing your small improvements first and discovering your solution while coding it, that seems really amazing! After some time testing and trying different logics, you find a possible way to go, and you say: "Yes! That's possible!"

As you can see, when using *TDD* then first that must be decided is *WHAT* to do, if that is clear and concrete, then you can try to solve it, experimenting with different solutions, even dumb and simple solutions are valid at first, then you can build a more complex solution, take baby steps and don't rush the code.

> The main thing you need to know at first is not HOW, but WHAT to do.

### How to use TDD?

The TDD cycle can be described as simples steps, followed until you find the final solution, or at least a satisfactory one:

1. **Write a test.** Get the final result you want and use it as an assertion, invent the interface you wish you had, and include all the elements you imagine will be necessary to calculate the right answer, don’t focus on HOW but WHAT first.
2. **Make it compile.** The first blocker to focus on, before ever thinking how it runs, you need to make it compile first, so do it.
3. **Run it to see that it fails.** After compiling, see your tests breaking, that’s you want to happen now.
4. **Make it run.** Get the test pass with the simplest and dumbest solution possible, don’t try to elaborate a complex solution at first.
5. **Make it right.** Now that the test pass, try to make it better creating abstractions and removing duplication. Take risks and make sure your test continues to pass.

The steps you want to achieve during the process are:

1. **Red** — Write a little test that doesn’t work, and perhaps doesn’t even compile at first.
2. **Green** — Make the test work quickly, committing whatever sins necessary in the process.
3. **Refactor** — Eliminate all of the duplication created in merely getting the test to work.

![TDD Cycle](https://miro.medium.com/max/2000/0*xdsM4xG4h3Z4M-pM.png)

> TDD is done by *Fail -> Pass -> Refactor* cycles, make it in baby tests and don’t rush the code. You’ll discover (and test) solutions during the process.

### When NOT to use TDD?

1. **Test-driven development is not acceptance testing.** You are testing small pieces of code, but not the external application behavior. For that, you can rely on automated tools such as _Cucumber_ or _Capybara_. Acceptance testing can be integrated with classic TDD, and it can serve as an extension of it.
2. **When you don't know WHAT to test.** Sometimes you are even discovering the interface and requirements of your application, for that case it can be better to code first, with that approach you can have ideas, and just getting into the flow can help you to clarify things.
3. **You are doing SPIKE coding.** When you're just testing a new API or trying a new integration as a test-of-proof, maybe it's not the time to do TDD yet. In that phase, you're trying different angles, and make mistakes are natural, after knowing clear requirements and interface, then TDD can help more.
4. **View testing.** Creating a visual feature can be a very creative and intuitive work, maybe you don't know the interface until it's done. After finishing it, you can think about how to test your outcome, but trying to test it first can block your creative mindset.

### Conclusion

TDD is a powerful tool and can really help you as a tool in your arsenal, such as a cooking chief who has the right tools to make a perfect meal. Rails community discusses recently if TDD's design benefits are even valuable, but usually, it brings smaller, clearer, and modular classes that result in less error-prone and better code quality. TDD is not a replacement for classic testing techniques, it's still possible to build bad code using it, but it's a valuable tool to be considered to help you to deliver better work.