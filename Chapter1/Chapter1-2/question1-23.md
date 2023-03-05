# Answer

### 1.
    1> (define (next n)
         (if (= n 2)
             3
             (+ n 2)))
    2> (define (find-divisor n test-divisor)
         (cond ((> (square test-divisor) n) n)
               ((divides? test-divisor n) test-divisor)
               (else (find-divisor n (next test-divisor)))))

### 2.
    No, Not 2 but roughly 1.5
    This is because if statements are additionally executed during the execution of procedure next.
    ==> This Answer is from http://community.schemewiki.org/?sicp-ex-1.23