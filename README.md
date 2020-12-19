# Digit-factorials
I use dictionary to make efficient operation

factorial_dictionary={0:1,1:1,2:2,3:6}

def factorial(n):
    if n in factorial_dictionary:
        return factorial_dictionary[n]
    else:
        result=n*factorial(n-1)
        factorial_dictionary[n]=result
        return result
t=1
for i in range(1,1000000000):
    i_str=str(i)
    l=len(i_str)
    sum=0
    for i in range(l):
        n=int(i_str[i])
        sum=sum+factorial(n)
    if t==sum:
        print(t)
    t+=1
