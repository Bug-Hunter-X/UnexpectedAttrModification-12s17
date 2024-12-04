# Ruby Getter Method Modification Bug

This repository demonstrates a subtle bug related to how getter methods work in Ruby.  Many programmers new to the language (or coming from other languages) assume that a getter implicitly allows modification of the internal state.  This is incorrect in Ruby.

## The Bug

The `bug.rb` file shows a `MyClass` with a getter `value`. Attempting to change the value via the getter (`my_object.value = 20`) does not modify the object's internal `@value` attribute.

## The Solution

The `bugSolution.rb` file corrects this by introducing a setter method (`value=`). Setters are explicitly designed to allow modification of the internal state of an object. This is a crucial difference that prevents accidental data corruption or unexpected behavior.