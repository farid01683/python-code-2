#######while

a = [1,2,3,4,5,6]
b = 0
i = 0
c = len(a)
while i <c:
    b = b + a[i]
    i = i + 1
    print(b)




a= [-10,1,2,3,4,5]
i=0
while i<len(a):
      if a[i] <0:
          a[i]=0
      i= i+ 1
print(a)


#########set 


a = {1,2,3,4}
b= {2,4,5,6}
c= a.intersection(b)
print(c)
d= a.union(b)
print(d)


