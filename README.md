I'm John o, the author. 
Example is given below with the length of the sequences to be 48. There is a pattern observed when doing 24 iterations of the o-output on the Fibonacci sequences. Check print in Python IDE and check data. 
J is pre-allocated. then the following code:

for thing in zz:
    myfunc(thing)
    j.append(myfunc(thing))
This produces the pattern. Every 24 numbers will produce a Fibonacci pattern that repeats twice since length is 48. 1,1,2,3,5 ... , F_48
-----------------
x = [1,1]

for i in range(48):
    y = int( x[i] + x[i+1])
    x.append(y)
    
zz = []
for element in range(len(x)):
    z = str(x[element])
    zz.append(z)

print("here is the fib seq, aka x: ",x)
print(" it has length: ", len(x))


def myfunc(put):
    output = 0
    for elementz in range(len(put)):
        output += int(put[elementz])
    if output > 9:
        return myfunc(str(output))
    elif output == 9:
        return str(9)
    else:
        return str(output)

j = []
for thing in zz:
    j.append(myfunc(thing))
print("here is the oo of sequence: ",j)
#y = j + 9 n we have y and j, solve for n for each number in the fibbonaci sequence
#y 1 1 2 3 5 8 13 21 34 55
#j  1 1 2 3 5 8 4   3    7    1
#n 0 0 0 0 0 0 1 2 3 6 
# n = (y-j)/9 
npower = []
#x and j have same length lists, different type of element in lists, int vs. str

for eachfib in range(len(x)):
   n = (x[eachfib] - int(j[eachfib]))//9
   npower.append((n))
print("this is n: " ,npower)

fibproof = []
for ihat in range(len(x)):
    fibproof.append(9*int(npower[ihat]) + int(j[ihat]))
print(fibproof)