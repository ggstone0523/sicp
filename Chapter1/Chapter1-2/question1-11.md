# Answer

### 1.
    1> (define (f n)
         (cond ((= n 0) 0)
               ((= n 1) 1)
               ((= n 2) 2)
               (else (+ (f (- n 1)) (* 2 (f (- n 2))) (* 3 (f (- n 3)))))))
    
    #recursive process

### 2.
    1> (define (f n)
         (f-iter 2 1 0 n))
    2> (define (f-iter a b c count)
         (cond ((= count 0) c)
               ((= count 1) b)
               (else (f-iter (+ a (* 2 b) (* 3 c)) a b (- count 1)))))

    #iterative process