# Answer

### 1.
    1)
    a <= bq + aq + ap
    b <= bp + aq

    2)
    a <= bpq + aq^2 + bq^2 + aq^2 + apq + bpq + apq + ap^2
    b <= bp^2 + apq + bq^2 + aq^2 + apq

    a <= b(2pq + q^2) + a(2pq + q^2) + a(p^2 + q^2)
    b <= b(p^2 + q^2) + a(2pq + q^2)

    p' == (p^2 + q^2)
    q' == (2pq + q^2)

### 2.
    1> (define (fib n)
         (fib-iter 1 0 0 1 n))
    2> (define (fib-iter a b p q count)
         (cond ((= count 0) b)
               ((even? count)
                (fib-iter a
                          b
                          (+ (* p p) (* q q))
                          (+ (* 2 (* p q)) (* q q))
                          (/ count 2)))
               (else (fib-iter (+ (* b q) (* a q) (* a p))
                               (+ (* b p) (* a q))
                               p
                               q
                               (- count 1)))))
