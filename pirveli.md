

# LISTS
```python
a = [1,2,3]
-----------------------------------------
a = [1,
	2,3,4,
	5,6]
-----------------------------------------
a = [1, #item 1
	2, #item 2]

```
# TUPLES
```python
a = (1 #comment
	,2 #comment
	,3 #comment)

```

#  SETS
```python
a = {'key1' : 1 #value for key 1
	,'key2': 2 #value for key 2
	}
#ვხურავთ ქვევით

```
# FUNCTION
```python
def my_func(a, #this is used to indicate....
			b, #comment
			c)
	print(a,b,c)
my_func(10,20,30)
my_func(10,
		20,
		30)
my_func(10, #comment
		20, #comment
		30)
```
# IF STATEMENT
```python
a = 10
b = 20
c = 30
if a > 5 \
	 and b > 10 \
	     and c < 20:
	print('yes')
```
# MULTI-LINE STRINGS
```python
a = ''' this is a string '''

a = ''' this\nis a string '''

a = ''' some items:
		1. item 1
		2. item2'''
print(a)
---------------------------------------------------------
def my_func():
	a = '''a multi-line string
	that is indented in the second line'''
	return a
print(my_func())
```
# CONDITIONALS
```python
a = 6

if a < 5:
	print('a < 5')
else:
	print('a > 5')
-------------------------------------------------

a = 10

if a < 5:
	print('a < 5')
else:
	if a < 10:
		print('5 <= a < 10')
	else:
		print('a >= 10')
--------------------------------------------------
a = 25

if a < 5:
	print('a < 5')
elif a < 10:
	print('5 <= a < 10')
elif a < 15:
	print('10 <= a < 15')
else:
	print('a > 15')
--------------------------------------------------
a = 25

if a < 5:
	b = 'a < 5'
else:
	b = 'a >= 5'
print(b)

b = 'a < 5' if a < 5 else 'a >= 5'
print(b)
```

# FUNCTIONS
```python
s = [1,2,3]
len(s)
--------------------------------------------------
from math import sqrt
sqrt(4)
--------------------------------------------------
import math
math.pi
math.exp(1)
--------------------------------------------------
def func_1():
	print('running func_1')

func_1()
--------------------------------------------------
def func_2(a: int, b: int):
	return a * b

func_2(2,3)
func_2('a',3)
func_2([1,2], 3)
func_2('a', 'b') #TypeError
--------------------------------------------------
def func_3():
	return func_4()
def func_4():
	return 'running func_4'

func_3()
--------------------------------------------------
def func_5():
	return func_6()

func_5()

def func_6():
	print('running func_6)
	#NameError
--------------------------------------------------
my_func = func_4
func_4()
my_func()
--------------------------------------------------
lambda x: x**2

fn1 = lambda x: x**2
fn1(2)
```

# WHILE LOOP
```python
i = 0
while i < 5:
	print(i)
	i += 1
--------------------------------------------------
i = 5

while True:
	print(i)
	if i >= 5:
		break
--------------------------------------------------
min_length = 2
name = input("please enter your name:")
while not(len(name) >= min_length and name.isprintable() and name.isalpha()):
	name = input("please enter your name:")
	
--------------------------------------------------
print("Hello, {0}".format(name))

min_length = 2
while True:
	name = input("please enter your name:")
	if (len(name) >= min_length and 		name.isprintable() and name.isalpha()):
		break
	
	
print("Hello, {0}".format(name))
--------------------------------------------------
a = 0
while a < 10:
	a += 1
	if a % 2 == 0:
		continue
	print(a)
--------------------------------------------------
l = [1,2,3]
val = 10

found = False
idx = 0
while idx < len(l)
	if l[idx] == val:
		found = True
		break
	idx += 1

if not found:
	l.append(val)
print(l)
--------------------------------------------------
l = [1,2,3]
val = 10
idx = 0

while idx < len(l):
	if l[idx] == val:
		break
	idx += 1
else:
;	l.append(val)
print(l)

```
# BREAK, CONTINUE AND TRY STATEMENT
```python
a = 10
b = 0
try:
	a/b
except ZeroDivisionError:
	print('division by 0')
finally:
	print('this always executes')
--------------------------------------------------

a = 0
b = 2
while a < 4:
	print('----------------')
	a += 1
	b -= 1

	try:
		a/b
	except ZeroDivisionError:
		print("{0}, {1} = division by 0".format(a,b))
		continue
	finally:
		print("{0}, {1} - always executes".format(a,b))
		
	print("{0}, {1} - main loop".format(a,b))
--------------------------------------------------

a = 0
b = 10
while a < 4:
	print('----------------')
	a += 1
	b -= 1

	try:
		a/b
	except ZeroDivisionError:
		print("{0}, {1} = division by 0".format(a,b))
		break
	finally:
		print("{0}, {1} - always executes".format(a,b))
		
	print("{0}, {1} - main loop".format(a,b))

else:
	print('Code executed without a zero division error')
```

# THE FOR LOOP
```python
for (int i = 0; i < 5;i++) {...}

i = 0
while i < 5:
	print(i)
	i += 1
i = None
--------------------------------------------------

for i in range(5):
	print(i)
--------------------------------------------------
for i in [1,2,3,4]:
	print(i)
--------------------------------------------------
for x in ('a', 'b', 'c', 4):
	print(x)
--------------------------------------------------
for i,j in [(1,2), (3,4), (5,6)]:
	print(i,j)
--------------------------------------------------
for i in range(5):
	if i == 3:
		break
	print(i)
--------------------------------------------------
for i in range(1,8)
	print(i)
	if i % 7 == 0:
		print('multiple of 7 found')
		break

else:
	print('no multiples of 7 in thge range')
--------------------------------------------------
for i in range(5):
	print('----------------')
	try:
		10/(i-3)
	except ZeroDivisionError:
		print('divided by 0')
		continue
	finally:
		print('always run')

	print(i)
--------------------------------------------------

s = 'hello'
for c in s:
	print(c)
--------------------------------------------------
s = 'hello'
i = 0
for c in s:
	print(i,c)
	i += 1 
--------------------------------------------------
s = 'hello'

for i in range(len(s)):
	prin(i, s[i])
--------------------------------------------------
s = 'hello'

for i, c in enumerate(s):
	print(i,c)
	
```

# CLASSES
```python
class Rectangle:
	def __init__(self, width, height):
		self.width = width
		self.height = height

r1 = Rectangle(10, 20)
r1.width
r1.width = 100
r1.width #შეგვიძლია გარეთ შეცვლა
--------------------------------------------------
class Rectangle:
	def __init__(self, width, height):
		self.width = width
		self.height = height

	def area(self):
		return self.width * self.height

	def perimeter(self):
		return 2 * (self.width + self.height)

r1 = rectangle(10,20)
r1.area()
r1.perimeter()
--------------------------------------------------
class Rectangle:
	def __init__(self, width, height):
		self.width = width
		self.height = height

	def area(self):
		return self.width * self.height

	def perimeter(self):
		return 2 * (self.width + self.height)

	def __str__(self): #აბრუნებს სტრინგს
		return 'Rectangle: width={0}, height={1}'.format(self.width, self.height)
	
	def __repr__(self):
		return 'Rectangle({0}, {1}'.format(self.width, self.height)

r1 = Rectangle(10,20)
r2 = Rectangle(10,20)
r1 is not r2 #True
r1 == r2 #False
str(r1)

--------------------------------------------------

class Rectangle:
	def __init__(self, width, height):
		self.width = width
		self.height = height

	def area(self):
		return self.width * self.height

	def perimeter(self):
		return 2 * (self.width + self.height)

	def __str__(self): #აბრუნებს სტრინგს
		return 'Rectangle: width={0}, height={1}'.format(self.width, self.height)
	
	def __repr__(self):
		return 'Rectangle({0}, {1}'.format(self.width, self.height)

	def __eq__(self, other):
		return self.width == other.width and self.height == other.height

r1 = Rectangle(10,20)
r2 = Rectangle(10,20)
r1 is not r2 #True
r1 == r2 #True
--------------------------------------------------
class Rectangle:
	def __init__(self, width, height):
		self.width = width
		self.height = height

	def area(self):
		return self.width * self.height

	def perimeter(self):
		return 2 * (self.width + self.height)

	def __str__(self): #აბრუნებს სტრინგს
		return 'Rectangle: width={0}, height={1}'.format(self.width, self.height)
	
	def __repr__(self):
		return 'Rectangle({0}, {1}'.format(self.width, self.height)

	def __eq__(self, other):
		if isinstance(other, Rectangle):
			return self.width == other.width and self.height == other.height
		else:
			return False
			
	def __lt__(self,other):
		if isinstance(other, Rectangle):
			return self.area() < other.area()
		else:
			return NotImplemented

r1 = Rectangle(10,20)
r2 = Rectangle(100, 200)
r1 < r2 #True
r2 < r1 #False
r2 > r1 #True

--------------------------------------------------
class Rectangle:
	def __init__(self, width, height):
		self.width = width
		self.height = height

	def __str__(self): #აბრუნებს სტრინგს
		return 'Rectangle: width={0}, height={1}'.format(self.width, self.height)
	
	def __repr__(self):
		return 'Rectangle({0}, {1}'.format(self.width, self.height)

	def __eq__(self, other):
		if isinstance(other, Rectangle):
			return self.width == other.width and self.height == other.height
		else:
			return False
r1 = Rectangle(10,20)
r1.width #10
r1.width = -100
r1.width #-100
r1 #Rectangle(-100,20)

--------------------------------------------------
class Rectangle:
	def __init__(self, width, height):
		self._width = width
		self._height = height #პრაივეითი, მაგრამ შეცვლა შეიძლება
	
	def get_width(self):
		return self._width

	def set_width(self, width):
		if width <= 0:
			raise ValueError("width must be positive.")
		else:
			self._width = width
			
	def __str__(self): #აბრუნებს სტრინგს
		return 'Rectangle: width={0}, height={1}'.format(self._width, self._height)
	
	def __repr__(self):
		return 'Rectangle({0}, {1}'.format(self._width, self._height)

	def __eq__(self, other):
		if isinstance(other, Rectangle):
			return self._width == other._width and self._height == other._height
		else:
			return False
			
r1 = Rectangle(10.20)
r1.width #AttributeError
r1.width = -100
r1.width #-100
r1._width #10
r1 #Rectangle(10,20)
r1.get_width() #10
r1.set_width(-10) #width must be positive

--------------------------------------------------
class Rectangle:
	def __init__(self, width, height):
		self.width = width
		self.height = height
	
	@property
	def width(self):
		print('getting width')
		return self._width
	
	@width.setter
	def width(self.width):
		if width <= 0:
			raise ValueError('width must be positive')
			else:
				self._width = width
		
	@property
	def height(self):
		self._height
	
	@heigh.setter
	def heigh(self.heigh):
		if width <= 0:
			raise ValueError('heigh must be positive')
			else:
				self._heigh = heigh
			
	def __str__(self): #აბრუნებს სტრინგს
		return 'Rectangle: width={0}, height={1}'.format(self.width, self.height)
	
	def __repr__(self):
		return 'Rectangle({0}, {1}'.format(self.width, self.height)

	def __eq__(self, other):
		if isinstance(other, Rectangle):
			return self.width == other.width and self.height == other.height
		else:
			return False

r1 = Rectangle(10,20)
r1.width #10
r1.width = -100 #Width must be positive


```

