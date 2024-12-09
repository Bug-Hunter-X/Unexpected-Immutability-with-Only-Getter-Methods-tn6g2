# Ruby Getter-Only Bug

This example demonstrates a common misunderstanding in Ruby regarding getter methods.  When you only define a getter method for an instance variable, the instance variable behaves as if it's immutable from outside the class.  The code attempts to change the value, but the change is not reflected.

## How to Fix

To make the instance variable modifiable, you need to define either a setter method (using `attr_writer`, `attr_accessor`, or explicitly defining a setter method) or use instance_variable_set within the class.