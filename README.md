
# hellolisp.rb
a mini Lisp interpreter in Ruby

### supports

`let` `lambda` `defun` `quote` `if`

and some [library functions](https://github.com/airtial/hellolisp.rb/blob/master/src/Library.rb)

### usage

    $ ruby src/Hellolisp.rb lispcode.l

or

```ruby
require 'src/Hellolisp.rb'

code = <<-'EOC'
  (defun foo (x) (+ x 1))
  ((lambda (x) (* x (foo x))) 2)
EOC
actual = Hellolisp::eval(code)
```

### references

Thank you to [Mary Rose Cook](http://maryrosecook.com/) [(Little Lisp interpreter)](https://www.recurse.com/blog/21-little-lisp-interpreter)

### more

[hellolisp.scala](https://github.com/airtial/hellolisp.scala) (implementation in Scala)
