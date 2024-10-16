## Dynamic programming:
- It is used to solve complex problems by breaking into small subproblems and store result in each stage to avoid redudants.
- USES
	 - Optimal Substructure
	 - Overlapping subproblems
- APPROACHES
	 - Top-Down (memoization) ->start with final solution and recursively solve it
	 - Bottom-Up (tabulation) ->start with smallest subproblems and gradually build the final result.
### Problem

```python

## Normal recursive method
def fibo(n):
	 if n<=1:
		 return n
	 else:
		 return fibo(n-1)+fibo(n-1)
if __name__=='__main__':
	n=10
	print(fib0(5))
```


- MEMOIZATION

```python
  Fibo=[]
  def fibo(n):
	  if n in Fibo:
		  return Fibo[n]
	  elif n<=1:
		  res=n 
	  else:
		  res=fibo(n-1)+fibo(n-2)
	  Fibo[n]=res
	  return res
 n=10
 print(fibo(n))

```
