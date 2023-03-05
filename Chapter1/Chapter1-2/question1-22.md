# Answer

### 1.
    1> (define (search-for-primes start end)
         (timed-prime-test start)
         (if (< start end)
             (search-for-primes (+ start 1) end)))
    
### 2.
    1000    : 1009, 1013, 1019
    10000   : 10007, 10009, 10037
    100000  : 100003, 100019, 100043
    1000000 : 1000003, 1000033, 1000037

    The calculation speed is fast, so there is amplitude, but it is generally about root of 10 times more. Therefore, it can be said that the time it takes to execute a program increases proportionally to the number of computational steps that grow.