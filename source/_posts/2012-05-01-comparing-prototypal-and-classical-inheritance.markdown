---
layout: post
title: "Comparing Prototypal and Classical Inheritance"
date: 2012-05-01 16:16
comments: true
categories: javascript, programming
---

Programmers familiar with the classic model of inheritance are often confused by JavaScript's prototypal inheritance when they first encounter it. To help illustrate the differences in the two models, I'll implement what might appear to be the same thing in both Ruby and JavaScript. 

<!-- more -->

In each example, I'll define a class `Foo` and a class `Bar` which inherits from `Foo`. It's worth noting that in JavaScript I am defining constructor functions, not classes (JavaScript has no class system). Then I'll create two instances of `Bar`. With the first instance, `baz`, I will

1. push the value `1` into its `a` property (an array)
- directly modify its `a` property to be the array `[1,2,3]`
- delete its `a` property entirely

After each step I will print out the state of each instance, at which point some drastic differences in the two programs will become apparent.

First, here's a simple example of class inheritance and instantiation in Ruby:
{% gist 2570770 inheritance-demo.rb %}

And here's what running that Ruby script outputs:
{% gist 2570770 ruby-output.txt %}

I create two instances, `baz` and `qux`. When I  modify properties on `baz`, properties on `qux` are not changed. This makes sense. 

Here is a comparable JavaScript program:
{% gist 2570770 inheritance-demo.js %}

The JavaScript program has a different output due to the fundamental differences in the two inheritance models.
{% gist 2570770 javascript-output.txt %}

Here are the differences highlighted.
{% gist 2570770 ruby-vs-javascript.diff %}

So, this raises a few questions:

- Why does `baz.a.push(1);` also modify `qux.a` in JavaScript? 
- Subsequently, why does `baz.a = [1,2,3];` not modify `qux.a`? 
- And why is `baz.a` still `1` after `delete baz.a;`?

Well, `baz` and `qux` do not have their own property `a`. Instead, they share `a` from their prototype. When I call `baz.a`, JavaScript first looks at `baz` for `a`, then it begins traversing the prototype chain upwards looking for a property `a` until it finds one, or returns `undefined` if it cannot. In the next step, I directly define a property `a` on `baz` which equals `[1,2,3]`. When I try to access it, JavaScript finds the property directly on `baz` and returns it. Then,
after `delete baz.a`, when `baz.a` is called again, JavaScript walks back up the prototype chain and finds the shared `a` on the prototype. 

*Unlike a class, which is like a blueprint for an instance, an object's prototype is itself another object.*

<figure>
<img src="/images/prototypal-console.png" />
<figcaption>
In the image above, baz and qux are created in the web inspector console and modified. Each instance has a visible `__proto__` reference pointing to its prototype, an instance of `Foo`. The `a` property is visible on the prototype, and it is visible on `baz` after it is directly defined as `[1,2,3]`.
</figcaption>

A prototype, being just an object, can be accessed and modified at runtime. 

<figure>
<img src="/images/prototypal-console-2.png" />
<figcaption>
In the image above, the prototype is directly modified at runtime.
</figcaption>


I hope this helps shed some light on what makes prototypal inheritance different from classical inheritance. Though some programmers want to emulate classical inheritance patterns in JavaScript, it is best to embrace prototypal inheritance, which offers its own expressive power. 

#### Further Reading

- [Prototypal Inheritance](http://javascript.crockford.com/prototypal.html)
- [Prototype-based Programming](http://en.wikipedia.org/wiki/Prototype-based_programming)
- [How to Node - Prototypal Inheritance](http://howtonode.org/prototypical-inheritance)
- [What the Fuck is Prototypal Inheritance](http://oscargodson.com/posts/what-the-fuck-is-prototypal-inheritance.html)
- [MDN](https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object/prototype)
