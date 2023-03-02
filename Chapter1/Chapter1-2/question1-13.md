# Answer

### 1.
    => (g^n / sqrt(5)) = Fib(n) + (t^n / sqrt(5))
    => -1 < t^n < 1
    => 2 < sqrt(5) < 3
    => -(1 / 2) < (t^n / sqrt(5)) < (1 / 2)
    => Fib(n) - (1 / 2) 
       < Fib(n) + (t^n / sqrt(5))
       < Fib(n) + (1 / 2)
    => Fib(n) - (1 / 2) 
       < (g^n / sqrt(5)) 
       < Fib(n) + (1 / 2)
    => So, Fib(n) is nearest integer to (g^n / sqrt(5))

    # This Answer is from 
      https://sicp-solutions.net/post/sicp-solution-exercise-1-13/

### 2.
    => Fib(1) = 1 is correct
    => Fib(n) = n suppose correct
    => Fib(n+2) - Fib(n+1) - Fib(n) = 0
    => ((g^2 * g^n) + (t^2 * t^n)) / sqrt(5)
       - ((g * g^n) + (t * t^n)) / sqrt(5)
       - (g^n + t^n) / sqrt(5)
       = (((g^2 - g - 1) * g^n) 
         + ((t^2 - t - 1) * t^n)) / sqrt(5)
    => g^2 - g - 1 = 0
    => t^2 - t - 1 = 0
    => g^2 = g + 1 is correct
    => t^2 = t + 1 is correct
    => So, Fib(n+2) - Fib(n+1) - Fib(n) = 0 is correct
    => And, Fib(n) = (g^n - t^n) / sqrt(5) is correct

    # This Answer is from
      https://math.stackexchange.com/questions/1933071/prove-by-induction-fibonacci-f-n-frac-left-frac1-sqrt-52-rightn-le 's
      second answer
