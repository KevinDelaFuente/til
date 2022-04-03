---
layout: post
title:  "Starting on the Path"
---
# TIL stands for "Today I Learned"
---
## Questions raised from _[The Ruby Koans](http://rubykoans.com/):_
---
### Questions from _about_arrays.rb_
- Is the syntax for ruby arrays array.[`index`, `#_of_elements`]? I think this is the case instead of a vector where the second argument is the _up to_ element you select in the array

### Questions from _about_strings.rb_
- How does `EOS` work? Can any string encapsulate another string?
- What do the `<<` do?
  - It actually  appends strings, but why does it modify also the `original_string`? is it because of `hi` = `original_string`?
- Why do we convert the list of symbols to strings and then compare against the string value rather than against symbols?

---

## _Here are (at least) three things I learned from [The Ruby Koans](http://rubykoans.com/):_
- Operators
  - Any non-false or non-nil object in Ruby will be evaluated as true, For example: 0, "", {}, are truthy.
  - Single quoted strings DO NOT interpret escape characther e.g., '\n' will have lenght of two vs "\n" length of one
  - Single quoted strings DO NOT, e.g., 'The value is #{value}'
  - eql? -> Unlike the == operator which tests if both operands are equal, the equal method checks if the two operands refer to the same object. This is the strictest form of equality in Ruby.
  
- Arrays
  - _unshift_ and _push_ add the first and last element of an array respectively
  - _shift_ and _pop_ remove the first and last element of an array respectively
  - Splat operator assigns the rest of elements to variable in parallel assignements: `first_nam`, *`last_name` = ["John", "Smith", "III"] will assign ["Smith", "III"] to `last_name`

- Objects
  - Object ID's for small integers follow a pattern of doubling the interger plus 1

-Hashes
  - Why might you want to use #fetch instead of #[] when accessing hash keys? -> Because fetch _will_ let you know there is  no key instead of returning `nil`
  - When creating a new hash, if there are values assigned in it without a key, it will automatically be assigned to any empty by default 

---
