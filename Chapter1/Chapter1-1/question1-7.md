# Answer

### 1.
    sqrt(0.0001) 
    correct answer   => 0.01
    evaluated answer => 0.03230844833048122

### 2.
    1> (define (improve guess x)
         (average guess (/ x guess)))
    2> (define (average x y)
         (/ (+ x y) 2))
    3> (define (good-enough? guess older-guess)
         (< (abs (- guess older-guess)) 0.001))
    4> (define (sqrt-iter guess x older-guess)
         (if (good-enough? guess older-guess)
             guess
             (sqrt-iter (improve guess x) x guess)))
    5> (define (sqrt x) (sqrt-iter 1.0 x 0))
    6> (sqrt 0.0001)
    .010000714038711746
    7> (sqrt 3)
    1.7320508100147274
