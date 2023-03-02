# Answer

### 1.
    1> (define (pascal-tri row term)
         (cond ((= 0 term) 1)
               ((= row term) 1)
               (else (+ (pascal-tri (- row 1) (- term 1))
                        (pascal-tri (- row 1) term)))))