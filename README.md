# Ruby Getter Method Assignment Bug

This repository demonstrates a common error in Ruby where assigning a value to a getter method does not modify the underlying instance variable. The `bug.rb` file showcases this issue, and `bugSolution.rb` provides the correct solution.

## Bug Description:

The issue arises when you mistakenly attempt to change the state of an object by assigning a value through a method defined without the `=` operator.  This method is treated only as a getter, not as a setter.  As a result, the assignment has no effect. This is a subtle error that can lead to unexpected behavior and difficult-to-debug issues.

## How to Reproduce:

1. Clone this repository.
2. Run `ruby bug.rb`.
3. Observe that the value of the instance variable remains unchanged after the attempted assignment through the getter method.

## Solution:

The `bugSolution.rb` file demonstrates the correct approach.  To modify the instance variable, you need to define a `setter` method explicitly using the `=` operator in the method signature.