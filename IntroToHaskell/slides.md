# Intro to Haskell 
---

# Haskell, writ bulleted

- Statically typed 
- Purely Functional
- Lazy

---

# Sin taxes

Things that do not do what you think they do:

- `.`   function compostion 
- `(` `)`   think order of operations
- `:`   singleton list append (throw an element on the front of a list)
- `$`   used to change the order of exectution
- `!=`  equivalent is `\=`
- `--`  actually a one line comment, like `//`
- `++`  not an incrementer (that wouldn't really make sense anyway)
        actually list join
- `%`   not used `mod` is what you want 

Things that do what you'd expect:

- Most math operations: `+` `-` `*` `/`
- Most boolean operators: `==` `&&` `||` `>` `<` `<=` `>=` 
- 
---

# Syntax you've been gone
Handy things in haskell

- `--` one line comment
- `(` `)` think math order of operations , not argument holders
- `:` singleton append, that is, if you have some list `xs` and some element 
    `x`, `x:xs` adds `x` to the front of `xs`
- `++` - joins a list

---

# Just not your type
## (Type signatures and declaration)

in Java:

    !java

    String str;

    char fname(int x){
        ...
        method definition
        ...
        return result;
    }

in Haskell:

    !haskell

    str :: String
    str = ""

    fname :: Int -> Char 
    fname x = ... function definition ...

---

# Loops! 

Just kidding

---

# Maps! 
Just cartography

Apply a given function to every element of a list. 

in Java:
    !java

    E func(E arg){
     // what your function does
     return arg;
    }

    ArrayList<E> map(ArrayList<E> list){
        for( E elem : list)
             func(elem);
        return list;
    }

in Haskell:
    
    !haskell

    func = -- whatever this does

    map func list

---

# I need a filter 

So suppose you have a list (or array) and you want to remove the elements that 
fail a condition.

in Java:

    !java
    ArrayList<Integer> filter(ArrayList<Integer> list){
        ArrayList<Integer> result = new ArrayList<Integer>();
        for( int a : list)
            if( test(a) == True)
                result.append(a)
        return result;
    }

in Haskell:

    !haskell
    filter :: (a -> Bool) -> [a] -> [a]
    
    filter test [] = []
    filter test (x:xs)
        | test x    = x : filter test xs
        | otherwise = filter test xs

##Presenter Notes

this is the actual implementation of filter in haskell
---

# Folding, at home!

Find the sum of the numbers from 1 to some number `n`. 

in Java:

    !java
    public int factorial(int n){
        int sum = 0;
        for(int i=0; i <n; i++){
            sum += i;
            }
        return sum;
    }

in Python:

    !python
    def factorial(n):
        sum = 0
        for i in range(1, n):
            sum += n
        return sum

---

# Folding, at home!

in Haskell:

    !haskell
    factorial n = foldl (+) [1 .. n]
---



---

# Resources

- [Learn you a Haskell](http://learnyouahaskell.com) - Great beginner resource
- [Real World Haskell](http://book.realworldhaskell.org/read/) - Another good book
- [Project Euler](http://book.realworldhaskell.org/read/) - Good practice problems, not just for haskell
- [Hoogle](http://www.haskell.org/hoogle) - search haskell functions by type signature
- [haskell.org](http://www.haskell.org) - 
- 
