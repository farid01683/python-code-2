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

    
#####File Handling
import os
if os.path.exists('name.txt'):
    print('file found')
else:
    print('file not found')


    ###############

    import  pathlib

a = pathlib.Path('name.txt')

if a.exists():
    print('hello')

print(os.path.abspath('name.txt')) 
print(os.path.getsize('name.txt'))

with open('name.txt', 'r') as f:
    print(f.read(5))

 with open('name.txt', 'r') as f:
    print(f.tell())   

    
   

##############error handel

try:
    with open('nae.txt', 'r') as f:
        print(f.read())
except FileNotFoundError:
    print("file not found")
    

    try:
    with open('name.txt', 'r') as f:
        print(f.read())
    print(10/2)
    x = int('abc')
except ZeroDivisionError:
    print('error')
except FileNotFoundError:
    print("file not found")

except ValueError:
    print ('error')

    try:
    with open('name.txt', 'r') as f:
        print(f.read())
    print(10/2)
    x = int(8)
    print(x)
    j = [1,2,4]
    print(j[100])
except ZeroDivisionError:
    print('error')
except FileNotFoundError:
    print("file not found")

except ValueError:
    print ('error')
except IndexError:
    print('error in')



try:
    with open('name.txt', 'r') as f:
        print(f.read())
    print(10/2)
    x = int(8)
    print(x)
    j = [1,2,4]
    print(j[1])
    x= abaa
except ZeroDivisionError:
    print('error')
except FileNotFoundError:
    print("file not found")

except ValueError:
    print ('error')
except IndexError:
    print('error in')
except Exception as e:
    print('error', e)

    else:
    print('successful')

    finally:
    print('print hobei')


Else, Finally and Raise



    def a(x):
    if not x.endswith('.txt'):
        raise ValueError ("only .txt file is allowed")
    print('valid file')

a('csv.txt')

try:                            [Custom Exception Handling]
    a('csv.txt')
except Exception as e :
    print(e)



################Class and Object


class car:
    def __init__(farid):
         farid.brand = ""
         farid.model = ""

car1 =car()
car1.brand = "toyota"
car1.model = "korola"

print(car1.brand)
print(car1.model)
print(car1.brand,car1.model)

car2 = car()
car2.brand = "honda"
car2.model = "hino"

print(car2.brand)
print(car2.model)
print(car2.brand,car2.model)



class car:
    def __init__(farid, brand, model):
        farid.brand = brand
        farid.model = model


car1 = car('toyota', 'honda')
print(car1.brand)
print(car1.model)

class car:
    def __init__(farid, brand = "honda", model ="noha"):
        farid.brand = brand
        farid.model = model


car1 = car()
print(car1.brand)
print(car1.model)



class car:
    def __init__(farid, brand, model):
        farid.brand = brand
        farid.model = model

    def display_info(farid):
        print(f"car brand: {farid.brand}\n car model : {farid.model}")

car1 = car('toyota', 'honda')
print(car1.brand)
print(car1.model)
car1.display_info()



Class vs Instance Variable


class school:
    school_name = "ostad school"

    def  __init__ (self, name):
         self.student_name = name


sc1 = school('rahim')

print(sc1.school_name)
print(sc1.student_name)



class x:
    a = "dhaka"

    def  __init__ (b, titel):
         b.y = titel


m = x('rahim')
n = x('karim')

print(m.a)
print(m.y)
print(n.a,n.y)



class p:
    x = "dhaka"

    def  __init__ (b, titel):
         b.y = titel


m = p('rahim')
n = p('karim')
m.x ="barhatta"

print(m.x)
print(m.y)
print(n.x,n.y)




class p:
    x = "dhaka"

    def  __init__ (b, titel):
         b.y = titel


m = p('rahim')
n = p('karim')
#m.x ="barhatta"

p.x ="barhatta"

print(m.x)
print(m.y)
print(n.x,n.y)


##### check again
class r:
    p = "dhaka"

    def  __init__ (a, name, salary):
         a.x = name
         a.y = salary


    def farid (a):
        print(f"my name is: {a.x}\n my salary is : {a.y}")

    @classmethod
    def masud (new, name):
        new.p = name

m = r("rahim", 3000)
m.farid()
m.masud('abc company')
print(m.p)





#####Static Method


class school:
    school  = "ckp pilot"

    @staticmethod
    def grade(mark):
        if mark >= 90:
            return"a"
        else:
            return'f'
print(school.grade(95))



class school:
    schoolname  = "ckp pilot"

    def __init__(self, name, salary):
        self.name = name
        self._salary = salary

    def getsalary (self, password ):
        if password == "admin":
            print(ob1._salary)
        else:
            print('confidancial')

    def set (self, password, salary ):
        if password == "admin":
            self._salary = salary
            print(f"new salary : {self._salary}")
        else:
            print('confidancial')
ob1 = school("rahim", 30000)
ob2 = school("korim", 40000)


ob1.getsalary("123")

print(ob1._salary)
print(ob1.name)


#####random
import random
print(random.random())
print(random.uniform(5,10))
print(random.randint(1,100))
print(random.randrange(1,100,5))

a = ['farid','masud','rahat']
print(random.choice(a))
random.shuffle(a)
print(a)


import random


def pin():
    return random.randint(1000,9999)

print(f"your 4 digit pin is :{pin()}")
