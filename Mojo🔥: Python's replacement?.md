---
title: "Mojo🔥: Python's replacement?"
seoTitle: "Mojo🔥: Python's replacement?"
seoDescription: "For decades, Python has dominated the ML space with little to no competition. But can Mojo finally be the answer to Python's woes?"
datePublished: Mon May 08 2023 22:40:32 GMT+0000 (Coordinated Universal Time)
cuid: clhffezxk000208laaa19gcfw
slug: mojo-pythons-replacement
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1683584741397/f6ee26ea-b111-406e-ade7-31539e9d8dc1.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1683585531466/8154b827-f553-4aa3-b0d6-f6b712d2a2ca.png
tags: news, machine-learning, programming-languages, mojo, mojo-vs-python

---

For all those working in Machine Learning, Python was always a no-brainer. The vast amount of libraries it has that support ML-related work is unparalleled. Also, the relaxed syntax makes it easy for ML Engineers to focus on the task at hand, rather than memory allocation, datatype declaration, etc. This placed Python at the pinnacle of languages for ML.

Until now.

Although Python has incredible benefits, it suffers tremendously in one area- speed. For decades, C & C++ loyalists have laughed at Python, taunting it for being too slow. That's where [***Mojo***](https://www.modular.com/mojo) comes in.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683584972740/7aa1fd3a-fa48-4435-b91d-43d8196f0fba.jpeg align="center")

Now, I know what you're thinking, how would a new programming language compensate for the problems of an existing one? Wouldn't you have to wait for years until this new language has the diversity and quality of libraries available in Python? Well, going by the creators of Mojo, that's not the case.

Mojo was developed by [Modular](https://www.modular.com/), as a superset of Python which can be up to 35,000x faster. Being a superset of Python means that Mojo contains everything that Python already has, and adds more to it. You could even say that Mojo is Python++, but "++" isn't valid in Python, so let's just stick to Mojo for now.

## Origin of Mojo

All good movie characters have a backstory. Mojo's backstory begins with Jeremy Howard, the founder of [***fast.ai***](https://www.fast.ai/). Years ago, when Jeremy first met Chris Lattner, he expressed his disappointment with the existing languages because of their poor performance. Jeremy wanted to be able to write performant, flexible and hardcore code, which is also concise, readable and understandable. To this, Chris replied, "Don't worry Jeremy. One day, we're going to fix this."

If you don't already know, Chris Lattner is the founder of Modular, creator of ***Swift*** (the language whose very name depicts its impeccable performance), and the ***LLVM*** compiler toolchain, which is a library that is used to produce intermediate or machine code. With those kinds of credentials, who better to fix Python's woes?

## But how is it so fast?

Mojo was designed for programming on AI Hardware like GPUs running ***Cuda*** (a general-purpose parallel computing platform and programming model developed by Nvidia, used to accelerate compute-intensive applications) and other accelerators. It achieves this by leveraging ***Multi-Level Intermediate Representation*** ***(MLIR)***.

What is MLIR, you ask? IR or ***intermediate representation*** is the data structure or code used internally by a compiler or virtual machine to represent source code in a low-level language that can be executed by the computer's hardware. This process involves multiple steps, and in each step, the representation of the program changes. The representation is "multi-level" because it includes representations at different levels of abstraction, from high-level language constructs to low-level hardware instructions.

Along with MLIR, Mojo even has built-in autotuning to optimize your code for your target hardware. That is, it detects the best parameters for your system automatically.

Mojo also adds strong type-checking. Although dynamic types are still usable, static types are a necessity for enhanced performance and memory management. It also enables the use of pointers as used in C++, along with the borrow checkers in Rust.

Jeff Delaney of [***fireship.io***](https://fireship.io/) put it best, "It's a pragmatic language that gives you safety but also the flexibility to be unsafe when needed".

## Ease of use

As mentioned earlier, Mojo was designed as a superset of Python in the same way TypeScript is a superset of JavaScript. So you can continue writing code in Python as usual, and learn the additional syntax of Mojo as you go along. This approach ensures a comparatively easy learning curve, which is much appreciated in a new language.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683585132155/989a1f5e-3bad-4a8e-92a4-f0f15f61059f.png align="center")

Mojo also has some similarities with JavaScript, with the usage of var and let declarations which can define mutable and immutable variables respectively. It also combines some C++ features like structs, while ensuring that the base language is fully compatible with Python.

As for the numerous Python libraries, Mojo can import these modules from the Python ecosystem and run them as usual. This, in my opinion, is what makes this language so special and exciting.

## Open-source?

Currently, Mojo is not available to the public. It's still in very early development it will be open-sourced in the future but currently there is a [waitlist](https://www.modular.com/mojo) to try it out.

Mojo's team stated on their [Github repo](https://github.com/modularml/mojo), "We plan to open-source Mojo progressively over time, but it's changing very quickly now. We believe that a small, tight-knit group of engineers with a shared vision can move faster than a community effort, so we will continue to incubate it within Modular until it's more complete."

## Coding in Mojo

To run Mojo code, you can create a file ending in .mojo or .🔥 which is a needless, yet cool little addition.

Python's def keyword for defining functions is replaced with fn which is a stricter type of function. We also see the usage of **Single Instruction Multiple Data (SIMD)** which is a built-in type that represents a vector where a single instruction can be executed across multiple elements in parallel on the underlying hardware.

## Conclusion

I'm really excited to see what Mojo has to offer, given all the claims that have been made by its creators. If they hold good, this could revolutionize the ML world.

But do you think Mojo can replace Python? Let me know in the comments section below.

If you liked this article, consider liking and sharing it, and please feel free to leave your thoughts, questions and ponderings in the comments.

You can also follow me for more data and ML-related content. I focus on demystifying technical jargon and encouraging newcomers in the field by explaining concepts as simply as possible.

This is Sachin being succinct :)
