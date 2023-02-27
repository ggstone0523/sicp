# Answer

### 1.
    (A 1 10)
    => 1024

    (A 2 4)
    => 65536

    (A 3 3)
    => 65536

### 2.
    (define (f n) (A 0 n))
    => 2n

    (define (g n) (A 1 n))
    => 2^n

    (define (h n) (A 2 n))
    => A(1) = 1
    => A(n) = 2^A(n-1) (n > 1)
    => 2^A(n)