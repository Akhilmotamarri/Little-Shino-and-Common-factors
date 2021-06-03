# Little-Shino-and-Common-factors
import time
import math
def factors(n):    
    result = set()
    for i in range(1, int(n ** 0.5) + 1):
        div, mod = divmod(n, i)
        if mod == 0:
            result |= {i, div}
    return result
n=list(map(int,input().split()))
a=n[0]
b=n[1]
gf=math.gcd(a,b)
print(len(factors(gf)))
