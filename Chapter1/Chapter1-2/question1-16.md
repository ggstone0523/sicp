# Answer

### 1.
    1> (define (even? n)
         (= (remainder n 2) 0))
    2> (define (fast-expt b n)
         (cond ((= n 0) 1)
               ((= n 1) b)
               (else (fast-expt-iter b n 1))))
    3> (define (fast-expt-iter b counter product)
         (if (= counter 1)
             product
             (cond ((even? counter) 
                    (fast-expt-iter b (/ counter 2) (* b b product)))
                   (else (fast-expt-iter b (- counter 1) (* b product))))))