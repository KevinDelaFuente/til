---
layout: post
title:  "Third Day on the Path to Ruby Enlightenment"
---

---
## _Here are the things I learned from [The Ruby Koans](http://rubykoans.com/):_

### Blocks
  - A block is the same thing as a method, but it does not belong to an object. Blocks are called closures in other programming languages. 

```
["Geeks", "GFG", 55].each {|i| puts i}  
```
```
Geeks
GFG
55
```

### Send
  - _send_ is a ruby (without rails) method allowing to invoke another method by name. For example:

```
   class Klass
     def hello(*args)
       "Hello " + args.join(' ')
     end
   end
   k = Klass.new
   k.send :hello, "gentle", "readers"   #=> "Hello gentle readers"
```


---

## Questions raised from _[The Ruby Koans](http://rubykoans.com/):_
---
### Questions from _about_blocks.rb_
- What exactly are blocks? What are the benefits of blocks over methods

### Quick notes from class about CRUD

  - find_by(:column =>value)
    - Same as .where().first
    - Can return a record of a nil if not record matches

  - find 
    - alwasys looks in ID column
    - Returns record
    - In production will return a 404



