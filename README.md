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



a = {"farrid" : 12, "munne": 11, 1:[1,2,3], 2: {1,3,4}}
for i in a:
    print(i)
for i in a.values():
    print (i)

    a = {"farrid" : 12, "munne": 11, 1:[1,2,3], 2: {1,3,4}}
for i in a:
    print(i)
for i in a.values():
    print (i)
print(a.keys(), a.values())

print("---------------------")

for c, d in a.items():
    print(f" name : {c}, values : {d}")


    
a= [1,2,3]
b= ["rahim", "karim", "hasan"]
print(list(zip(a,b)))
print(dict(zip(a,b)))


a= [1,2,3]
b= ["rahim", "karim", "hasan"]
c= list(zip(a,b))
print(c[0])

a= list(range(0,11))
b={i: "even" if i%2 == 0 else "odd" for i in a}
print(b)




a = input("what is your name?")
print ("hello",a)
b = max([1,2,3,4])
print(f"max value {b} . {b*2}")


def a():
    x = 10
    y= 15
    print (x+y)
a()


def a(x,y):
     print(x-y)

a(15,10)



def a(x,y):
  return x*y
z = a(5,6)
print(z)

def farid():
  return "farid"
c = farid()
print(c)

def a(*args):
    print(args)
    return sum(args)
r = a(3,4,5,6,7)
print(r)

Keyword Arguments


def a(x, y, z):
    print(f"myname is {x}, his name is {y}, age{z}")
a(x="farid", y="masud",z=23)


def a(**kwargs):
    print(kwargs)
a(x="farid", y="masud",z=23)


def a(**data):
    print(data)
a(x="farid", y="masud",z=23)
