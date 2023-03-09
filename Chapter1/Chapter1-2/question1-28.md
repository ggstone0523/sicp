# Answer

### 1.
    (define (expmod base exp m)
      (cond ((= exp 0) 1)
        ((nont base m) 0)
        ((even? exp)
         (remainder (square (expmod base (/ exp 2) m)) m))
        (else (remainder (* base (expmod base (- exp 1) m)) m))))
    (define (nont base n)
      (cond ((= base 1) #f)
        ((= base (- n 1)) #f)
        (else (= (remainder (square base) n) 1))))
    (define (fermat-test n)
      (define (try-it a)
        (= (expmod a (- n 1) n) 1))
      (try-it (+ 1 (randint (- n 1)))))
    (define (fast-prime? n times)
      (cond ((= times 0) #t)
        ((fermat-test n) (fast-prime? n (- times 1)))
        (else #f)))
    (define (randint . args)
      (cond ((= (length args) 1)
              (floor (* (random) (car args))))
            ((= (length args) 2)
              (+ (car args) (floor (* (random) (- (cadr args) (car args))))))
            (else (error 'randint "usage: (randint [lo] hi)"))))
    (fast-prime? 10 10)
    (fast-prime? 561 10)
    (fast-prime? 11 10)

    ==> randint procedure is from https://stackoverflow.com/questions/14674165/scheme-generate-random 's first answer
    ==> nont procedure's else-clause is from http://community.schemewiki.org/?sicp-ex-1.28
