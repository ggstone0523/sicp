# Answer

### 1.
    1> (define (square x) (* x x))
    2> (define (sum-of-squares x y)
         (+ (square x) (square y)))
    3> (define (>= x y) (or (> x y) (= x y)))
    4> (define (bigger-sum-of-squares x y z)
         (cond ((and (>= y x) (>= z x))
                (sum-of-squares y z))
               ((and (>= x y) (>= z y))
                (sum-of-squares x z))
               ((and (>= x z) (>= y z))
                (sum-of-squares x y))))