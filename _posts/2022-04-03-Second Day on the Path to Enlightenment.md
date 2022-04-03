---
layout: post
title:  "Second Day on the Path to Ruby Enlightenment"
---

---
## _Here are the things I learned from [The Ruby Koans](http://rubykoans.com/):_

### Regexp
  - **'Greedy'** means match longest possible string. For example: [/z*/], [/bc+/], [/ab?/]
  - **'Lazy'** means match shortest possible string.
  - 
  
  | **Shortcut** | **Meaning** |
  | \d | a digit |
  | \s | a whitespace including \t and \n |
  | \n | a return |
  | \t | a tab |
  | \w | a word including _ and digits |
  
  | **Character** | **Action** | **Example** |
  | ? | question_mark_means_optional | "abbcccddddeeeee"[/ab?/] -> 'ab' |
  | + | plus_means_one_or_more | "abbcccddddeeeee"[/bc+/] -> 'bccc'|
  | * | asterisk_means_zero_or_more | "abbcccddddeeeee"[/ab*/] -> 'abb' |
  |  |  |  |
  |  |  |  |
  
### Arrays
  - 
  - 
 

---

## Questions raised from _[The Ruby Koans](http://rubykoans.com/):_
---
### Questions from _about_constants.rb_
- Both nested class and subclasses inherit constants from enclosing and parent classes respectively. What are the differences between subclasses and nested classes 
- What is the inheritance hierarchy? What is the lexical scope?
- Why does the precedence change with specific scoping?



