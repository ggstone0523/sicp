# Answer

### 1.
    (define (expmod base exp m)
      (cond ((= exp 0) 1)
        ((even? exp)
         (remainder (square (expmod base (/ exp 2) m)) m))
        (else (remainder (* base (expmod base (- exp 1) m)) m))))
    (define (try-it a n)
      (= (expmod a n n) a))
    (define (check-carmichael n)
      (if (iter-cc (- n 1) n)
        #t
        #f))
    (define (iter-cc a n)
      (cond ((= a 0) #t)
        ((try-it a n) (iter-cc (- a 1) n))
        (else #f)))
    (check-carmichael 561)
    (check-carmichael 1105)
    (check-carmichael 1729)
    (check-carmichael 2465)
    (check-carmichael 2821)
    (check-carmichael 6601)
