# Answer

### 1.
    1> (define (double n)
         (+ n n))
    2> (define (halve n)
         (/ n 2))
    3> (define (* a b)
         (if (= b 0)
         0
         (cond ((= (remainder b 2) 0)
                (double (* a (halve b))))
               (else
                (+ a (* a (- b 1)))))))