
x = [1,1]
rs = 2
rsl = ['1','2']
for i in range(48):
    y = int( x[i] + x[i+1])
    rs += y
    x.append(y)
    rsl.append(str(rs))
zz = []
for element in range(len(x)):
    z = str(x[element])
    zz.append(z)

print("here is the fib seq, aka x: ",x)
print(" it has length: ", len(x))
#print("running sum is: ", rsl)
#make function that takes string of a number and outputs the sum of each digit in that number

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
    myfunc(thing)
    j.append(myfunc(thing))
print("here is the oo of sequence: ",j)
k = []
for member in rsl:
    myfunc(member)
    k.append(myfunc(member))
#print(k)

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
oon =[]
for eac in range(len(x)):
    oon.append(myfunc(str(npower[eac])))
print(oon)
# proof 9* n (i)+ oo(i) equals  fib sequence
fibproof = []
for ihat in range(len(x)):
    fibproof.append(9*int(npower[ihat] + int(k[ihat])))
print(fibproof)
