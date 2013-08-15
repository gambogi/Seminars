# Intro to Haskell
---

# Haskell, writ bulleted

- Statically typed 
- Purely Functional
- Lazy

---

# Loops

Just kidding.

---

# Just not your type
## (Type signatures and declaration)

in Java:

    !java
    int fname( int x, int y){
        ...
        method definition
        ...
        return result;
    }

in Haskell:

    !haskell
    fname :: int -> int -> int
    
    fname x y = ... function definition ...

---

# I need a filter 

So suppose you have a list (or array) and you want to remove the elements that 
fail a condition.

in Java:

    !java
    public ArrayList<Integer> filter(ArrayList<Integer> list){
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
