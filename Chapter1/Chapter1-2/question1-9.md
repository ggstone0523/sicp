# Answer

### 1.
    (define (+ a b)
        (if (= a 0)
            b
            (inc (+ (dec a) b))))

    => a = 3, b = 3
    => (+ 3 3)
    => (inc (+ 2 3))
    => (inc (inc (+ 1 3)))
    => (inc (inc (inc (+ 0 3))))
    => (inc (inc (inc 3)))
    => (inc (inc 4))
    => (inc 5)
    => 6

    => This process is recursive process

### 2.
    (define (+ a b)
        (if (= a 0)
        b
        (+ (dec a) (inc b))))

    => a = 3, b = 3
    => (+ 3 3)
    => (+ 2 4)
    => (+ 1 5)
    => (+ 0 6)
    => 6

    => This process is iterative process