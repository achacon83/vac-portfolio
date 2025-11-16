---
title: 'Clean Code'
description: 'A practical overview of core clean code principles and how to apply them in everyday development.'
pubDate: 'November 15, 2025'
heroImage: '../../assets/blog-placeholder-3.jpg'
---

Writing clean code is one of the most important skills for any software developer.  
It doesn’t matter how fast you can build something—if the code is hard to read,
bug-prone, or difficult to extend, the system will eventually slow you down.

In this post, I want to summarize a few principles I try to follow in my daily work.

## Meaningful Names
Good naming is the simplest and most effective way to make code readable.  
A name should clearly describe *why* it exists, *what* it does, and *how* it is used:

- `isActive` is better than `flag`
- `UserRepository` is better than `Handler`
- `calculateDiscount` is better than `process`

If a name needs a comment to be understood, the name is not good enough.
Avoid words whose entrenched meanings vary from our intended meaning:

- `hp`, `aix`, and `sco` would be poor variable names
- `accounts` is better than `accountList`

## Class Names
Classes and objects should have noun or noun-phrase names like `Customer`, `WikiPage`, and `Account`. Avoid words like `Manager`, `Processor`, `Data`, or `Info`. A class name should not be a verb.

Examples: `Customer`, `Order`, `Invoice`.

## Method Names
Methods should have verb or verb-phrase names like `postPayment`, `deletePage`, or `save`. Accessors, mutators, and predicates should be named for their value and prefixed with `get`, `set`, and `is` according to the JavaBeans standard.

When constructors are overloaded, use static factory methods with names that describe the arguments. For example:

`Complex point = Complex.fromRealNumber(23.0);`

## Small Functions
A function should do one thing and do it well.  
Small functions are easier to test, reason about, and maintain.

When a function grows too large, these are common symptoms:

- Too many parameters  
- Nested conditionals  
- Multiple responsibilities mixed together  

Extracting smaller functions usually improves clarity immediately.

## Avoid Duplication
Duplicated code is dangerous because fixing a bug in one place does not
guarantee it’s fixed everywhere else.

Whenever you see code being copied, it’s a good sign that you should:
- Extract a method  
- Create a utility  
- Introduce an abstraction  

Duplication increases the cost of maintenance over time.

## Fail Fast
Clean code makes invalid states impossible or easy to detect.

Examples:
- Validate inputs early  
- Throw exceptions instead of silently ignoring errors  
- Make illegal states unrepresentable with strong types  

Failing fast helps catch problems sooner and keeps the system predictable.

## Final Thoughts
Clean code is not about perfection.  
It’s about writing code that you and others can understand, modify, and extend
with confidence.

This is a continuous practice, and the goal of this blog is to document what I
learn as I try to apply these principles in real projects.
