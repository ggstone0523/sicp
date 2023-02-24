# Answer

### 1. 
applicative-order evaluation

    (test 0 (p))
    change (p) => (p) forever
    so, result is not show

normal-order evaluation

    (test 0 (p))
    (if (= 0 0) 0 (p))
    (if (#t) 0 (p))
    0
