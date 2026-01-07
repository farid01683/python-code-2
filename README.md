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


def a(**kwargs):
    print(kwargs)
    print(f"my name is {kwargs["x"]} your name {kwargs["y"]} age{kwargs["z"]} mark{kwargs["m"]} address{kwargs["n"]}")
a(x="farid", y="masud",z=23, m= 66, n="dhaka")


def a(**data):
    print(data)
    print(f"my name is {data["x"]} your name {data["y"]} age{data["z"]} mark{data["m"]} address{data["n"]}")
a(x="farid", y="masud",z=23, m= 66, n="dhaka")



Default Parameter and Pass Keyword



def x(a,b):
    print(a,b)
x("farid", "khan")


def x(a,b="khan"):
    print(a,b)
x("farid" )


a = lambda x: x*x
print(a(4))



x = [("farid",20), ("masud",30), ("rahat", 50)]
y = sorted(x, key = lambda m: m[1])
print(y)



a = [1,2,3,4]

y = list(map(lambda x:x*x,a))
print(y)
d = list(map( lambda  x : x%2 == 0,a))
print (d)
e = list(filter( lambda  x : x%2 == 0,a))
print (e)
m = functools.reduce(lambda x, y : x + y, a)
print(m)





##########Scope Resolution
x = 10

def a():
    x= 200
    def b():
        nonlocal x
        x= 300

        print(x)
    b()
a()

#######Reading from File


file = open('name.txt', 'r')
x =file.read()
print(x)


*file.close()


with open('name.txt', 'r') as f:
    x = f.read()
    print(x)
    
*write
with open('name.txt', 'w') as f:

    f.write("my name is rahat\n")
    f.write("my name is masud\n")


a =['i love python\n','i am new in python\n']

with open('name.txt','a') as d:
    d.writelines(a)    

    

import os
if os.path.exists('name.txt'):
    print('file found')
else:
    print('file not found')

