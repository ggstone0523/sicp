# Answer

### 1.
    1> (define (even? n)
         (= (remainder n 2) 0))
    2> (define (double n)
         (+ n n))
    3> (define (halve n)
         (/ n 2))
    4> (define (* a b)
         (acco-iter a b 0))
    5> (define (acco-iter a b counter)
         (if (= b 0)
             counter
             (cond ((even? b)
                    (acco-iter (double a) (halve b) counter))
                   (else
                    (acco-iter a (- b 1) (+ a counter))))))
    6> (define (fast-expt b n)
         (fast-expt-iter b n 1))
    7> (define (fast-expt-iter b counter product)
         (if (= counter 0)
             product
             (cond ((even? counter)
                    (fast-expt-iter (* b b) (/ counter 2) product))
                   (else
                    (fast-expt-iter b (- counter 1) (* b product))))))