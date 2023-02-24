# Answer

### 1.
    1> (define (improve guess x)
         (/ (+ (/ x (* guess guess)) (* 2 guess)) 3))
    2> (define (good-enough? guess older-guess)
         (< (abs (- guess older-guess)) 0.001))
    3> (define (cube-root-iter guess x older-guess)
         (if (good-enough? guess older-guess)
             guess
             (cube-root-iter (improve guess x) x guess)))
    4> (define (cube-root x) (cube-root-iter 1.0 x 0))
    5> (cube-root 8)
    2.000000000012062
    6> (cube-root 0.001)
    .10000000198565878
    7> (cube-root 125)
    5.000000000287929