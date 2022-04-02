---
layout: post
title:  "Starting on the Path"
---

### _about_strings.rb_
- How does `EOS` work? Can any string encapsulate another string?
- What do the `<<` do?
  - It actually  appends strings, but why does it modify also the `original_string`? is it because of hi = original_string?

TIL:
- Any non-false or non-nil object in Ruby will be evaluated as true, For example: 0, "", {}, are truthy.
- Single quoted strings DO NOT interpret escape characther e.g., '\n' will have lenght of two vs "\n" length of one
- Single quoted strings DO NOT, e.g., 'The value is #{value}'
