# CMPS 2200 Recitation 07
## Answers

**Name:** Menwe Okafor
**Name:**_________________________


Place all written answers from `recitation-07.md` here for easier grading.



- **2) (2 pts)** Write a recurrence for the **work** of this algorithm and solve it. Assume the input is $n$ to compute $F_n$.
  W(n) = W(n−1) + W(n−2) + 1. Every call makes two more calls, so the work basically doubles each time n goes up by 1. That makes it exponential, O(2^n).

- **3) (2 pts)** Write a recurrence for the **span** of this algorithm and solve it.
  If the two recursive calls run in parallel, we only wait on the longer one which is fib(n-1), So S(n) = S(n−1) + 1 = O(n).

- **4) (1 pt)** Inspecting the `counts` list, what interesting pattern emerges?
  The counts are the Fibonacci numbers backwards.

- **6) (2 pts)** When computing $F_n$, what is the maximum number of times that `fib_top_down(i)` will be called for any value $i$? Based on this, what is the **work** and **span** of this algorithm? 
  Each fib_top_down(i) gets called at most 2 times, once from i+1 and once from i+2. The second time it just returns the saved value. So there are about 2n calls that each do constant work, which makes the work O(n). The span is also O(n) because each value needs the ones before it, so they have to happen in order.


- **8) (2 pts)** When computing $F_n$, what is the maximum number of times that
  $F_i$ will be read from the list for any value $i$? Based on this, what is the **work** and **span** of `fib_bottom_up`?
    Each F_i gets read at most 2 times, once when computing F_(i+1) and once for F_(i+2). The loop runs n times with constant work each time, so the work is O(n). The span is O(n) too since every step depends on the previous two.
