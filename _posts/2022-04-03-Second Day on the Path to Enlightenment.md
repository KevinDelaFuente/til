---
layout: post
title:  "Second Day on the Path to Ruby Enlightenment"
---

---
## _Here are the things I learned from [The Ruby Koans](http://rubykoans.com/):_

### Regexp
  - **'Greedy'** means match longest possible string. For example: [/z*/], [/bc+/], [/ab?/]
  - **'Lazy'** means match shortest possible string.
  - Capitalize a shortcut to negate it. For example: \D, \S, \W
  
  | **Shortcut** | **Meaning** | **Example** |
  |:----------:|:--------------|:------|
  | \d | a digit | "the number is 42"[/\d+/] -> '42' |
  | \s | a whitespace including \t and \n | "space: \t\n"[/\s+/] -> " \t\n"|
  | \n | a return ||
  | \t | a tab ||
  | \w | a word including _ and digits | "variable_1 = 42"[/\w+/] -> 'variable_1' |
  | \A | anchors to the start of the string | "start end"[/\Astart/] -> 'start' |
  | \z | anchors to the end of the string | "start end"[/end\z/] -> 'end' |
  | \b | anchors to a word boundary | "bovine vines"[/\bvine./] -> "vines" |
  | scan | scan is like find all | "one two-three".scan(/\w+/) -> ["one", "two", "three"] |
  | sub | sub_is_like_find_and_replace | "one two-three".sub(/(t\w*)/) { $1[0, 1] } -> |
  
  | **Character** | **Action** | **Example** |
  |:-------------:|:-----------|:------|
  | ? | question_mark_means_optional | "abbcccddddeeeee"[/ab?/] -> 'ab' |
  | + | plus_means_one_or_more | "abbcccddddeeeee"[/bc+/] -> 'bccc' |
  | * | asterisk_means_zero_or_more | "abbcccddddeeeee"[/ab*/] -> 'abb' |
  | . | period_is_a_shortcut_for_any_non_newline_character | "abc\n123"[/a.+/] -> 'abc' |
  | ^ | negation of a character | "the number is 42"[/[^0-9]+/] -> 'the number is' |
  | ^ | caret_anchors_to_the_start_of_lines | "num 42\n2 lines"[/^\d+/] -> '2' |
  | $ | dollar_sign_anchors_to_the_end_of_lines | "2 lines\nnum 42"[/\d+$/] -> '42' |
  | () | parentheses_group_contents | "ahahaha"[/(ha)+/] -> 'hahaha' | 
  

### Control Operators
  - A ternary operator is made of three parts, that’s where the word “ternary” comes from. These parts include a conditional statement & two possible outcomes. In other words, a ternary gives you a way to write a compact if/else expression in just one line of code.

This...
```
if apple_stock > 1
  :eat_apple
else
  :buy_apple
end
```
Becomes this...
```
apple_stock > 1 ? :eat_apple : :buy_apple
```
 
### Iterations
  - Array.inject will pass each element of an array and will accumulate each sequentially
  - 
---

## Questions raised from _[The Ruby Koans](http://rubykoans.com/):_
---
### Questions from _about_constants.rb_
- Both nested class and subclasses inherit constants from enclosing and parent classes respectively. What are the differences between subclasses and nested classes 
- What is the inheritance hierarchy? What is the lexical scope?
- Why does the precedence change with specific scoping?

### Questions from _about_control_statements.rb_
- Difference between and && / or ||



