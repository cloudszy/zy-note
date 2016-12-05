# Pthon笔记

##容器篇
   * 列表list = [1,2,3.....]
  
      ```python

         zhiyi = ['a','b','c','d']
      ```
    [x * x for x in range(1, 11)]    
    

[x * x for x in range(1, 11) if x % 2 == 0]   
[m + n for m in 'ABC' for n in 'XYZ']








      * 新增 append()

       ```python
         zhiyi.append('e')
         zhiyi.append('f')
         zhiyi.append('g')
       ```
       [a,b,c,d,e,f,g]
      
      *  删除 pop()
    
       ```python
        zhuyi.pop('a')
        zhuyi.pop('b')
        zhuyi.pop('c')
       ```
       [d,e,f,g]
     
      * 插入 insert()
     
       ```python
           zhuyi.insert(0, 'a')
           zhuyi.insert(1, 'b')
           zhuyi.insert(2. 'c')
      ```
      [a,b,c,d,e,f,g]
     
      * 替换 
     
       ```python
          zhuyi[0] = 'q'
          zhuyi[1] = 'w'
          zhuyi[2] = 'e'
       ```
       [q,w,e,d,e,f,g]
     
   * 元组tuple = (1,2,3...)
     
       tuple,与list类似，但是tuple一旦生成初始化就不能修改。

       ```python

          zytupleyi = ('a','b','c')
       ```

       [a,b,c]
     
   * 字典dict，zydict = {1:'a',2:'b',3:'c'}
     
      * 增加 zydict[key] = value
       
       ```python

           zydict[4] = 'd'
       ```

       {1:'a',2:'b',3:'c',4:'d'}
      
      * 删除 zydict.pop()
       
       ```python
       
           zydict.pop(4)
           
       ```
       { 1:'a',2:'b',3:'c'}
       
      * 替换 zydict[key] = 'value'
      
        ```python
        
           zydict[3] = 'd'
           
       ```
       {1:'a',2:'b',4:'d'}

      * 查找 zydict[key]
       
       ```python
       
          zydict[1]
       ```
          b
 
      * 遍历 a_dict = {'a': 1, 'b': 2, 'c': 3} 
         
          * for in

          ```python

             for i in a_dict:
              print i,a_dict[i]

          ```
          a 1
          c 3
          b 2

          * items()

          ```python 

             for k, v in a_dictitems():
              print k, v

          ```

          * iteritems()

          ```python

            for k,  v in a_dict.iteritems():
             print k,v

          ```
         
          
          
   * set
     
     set和dict类似，也是一组key的集合，但不存储value。由于key不能重复，所以，在set中，没有重复的key.
     
     zhuyi = zhuyi([1,2,3])
      
      * 增加 zhuyi.add()
      
        ```python
        
           zhuyi.add(4)
        ```
        set([1,2,3,4])
        
      * 删除 zhuyi.remove()
        
        ```python
        
           zhuyi.remove(4)
           
        ```
        set([1,2,3])

## 条件与循环

      * if、else语句，如果if判断是False，不要执行if的内容，把else执行
      
         ```python
      
        age = 3
        if age >= 18:
         'your age is', age
         'adult'
        else:
          'your age is', age
          'teemager'

          ```
         your age is,age
         teemager
         
      * elif细致判断
         
         ```python
         
            age = 3
            if age >= 18:
              print 'adult'
                age >= 6:
                print 'teenager'
            else:
                print 'kid'
                
         ```
         kid
         
      * 循环 for...in
      
      ```python
      
         names = ['Michael', 'Bob', 'Tracy']
         for name in names :
            print name
            
      ```
      Michael
      Bob
      Tracy
      
      ```python
      
         sum = 0
         for x in range(101):
          sum = sum + x
         print sum
         
      ```
      5050
      
      * while循环，条件满足不断循环，条件不满足时退出循环
      
      ```python
      
        sum = 0
        n = 99
        while n > 0:
          sum = sum + n
          n =n - 2
        print sum
        
      ```
      2500
      
      * raw_input,结合int()装换整形
      
      ```python
      
         birth = (raw_input('birth:1982'))
         if birth < 2000:
          print '00前'
         else:
          print '00后'
          
      ```
      00前

##函数篇

      * 调用函数
     
     ```python
      
      abs(100)
      abs(-20)
      abs(12.34)

      ```
      100
      20
      12.34
      
      * 比较函数 cmp(x,y)
     
     ```python
     
        cmp(1,2)
        cmp(2,1)
        cmp(3,3)
        
     ```
         -1
          1
          0
          
      * 数据类型装换
      
      ```python
      
      int('123')
      int(12.34)
#      float('12.34')
      str(1.23)
      unicode(100)
      bool(1)
      bool('')
      
      ```
      123
      12
      12.34
      '1.23'
      u'100'
      Ture
      False

##定义函数

      * 空函数 pass
      
      ```python
      
        def nop():
        pass
        
      ```
      
      * 参数检查：数据类型检查 isinstance
      
      ```python
      
         def my_abs(x):
          if not isinstance(x, (int, float))
            raise TypeError('bad operand type')
           if x >= 0:
            return x
           else:
            retnrn - x
            
      ```
      my_abs('A')
      Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
      File "<stdin>", line 3, in my_abs
      TypeError: bad operand type    
      
      * 返回多个值,形参，实参
      
      ```python 
      
      def move(x, y, step, angle=0):
       nx = x + step * math.cos(angle)
       ny = y - step * math.sin(angle)
       return nx, ny
      x,y = move(100, 100, 60, math.pi/6)
      print x, y
      
      ```
      151,961524227 70.0
      
      ```python
      
      * 默认参数
      
      ```python
      
      def power(x):
        ruturn x * x
      print power(5)
      print power(15)
        
      ```
      25
      225
      
      ```python
      
      def power(x, n=2):
        s = 1
        while n > 0:
          n = n - 1
          s = s * x
        return
        print power(5, 2)
        print power(5,3)
      
      
      ```
      25
      125
      
      * 可变参数 *
      
      ```python
      
      def calc(*numbers):
        sum = 0
        for n in numvers:
          sum = sum + n * n
        return sum
        print calc(1, 2)
        print calc()
        
        ```
        5
        0
        
       *list
        
       * list、tpule，调用可变参数
       
       ```python
       
       nums = [1,2,3]
       print calc(nums[0], nums[1], nums[2])
       
       ```
       14
       
       ```python
       
       nums = [1,2,3]
       print calc(*nums)
       
       ```
       14
       
      * 关键字参数 **
      
      ```python
      
      def person(name, age, **kw):
        print 'name:', name, 'age:',age, 'ather:', kw
      print person('Michael', 30, city = 'beijing', gender = 'M')
      
      ```
      name: Michael age : 30 other: {'city': 'beijing', 'gender:' 'M'}
      
      * 关键词参数调用
        
        ```python 
        
        kw = {'city': 'beijing', 'job': 'Engineer'}
        print person('Jack', 24, **kw)
        
        ```
        Jack age : 24 othre : {'city': 'beijing', 'job': Engineer}
        
      * 参数组合 (顺序 必须参数、默认参数、可变参数、关键词参数) 
      
      ```python 
      
      def func(a,b,c = 0, *args, **kw)
        print 'a =', a, 'b =', b, 'c =', c, 'args =', args, 'kw =', kw
      print func(1, 2)
      print func(1, 2, c = 3)
      print func(1, 2, 3, 'a', 'b')
      print func(1, 2, 3, 'a', 'b', x = 99)
      
      ```
      a = 1 b = 2 c = 0 args = () kw = {}
      a = 1 b = 2 c = 3 args = () kw = {}
      a = 1 b = 2 3 args = ('a', 'b') kw = {}
      a = 1 b = 2 3 arhs = ('a', 'b') kw = {'x': 99}
      
     ```python
     
     agrs = (1,2,3,4)
     kw = {'x': 99}
     print func(*args, **kw)
     
     ```
     a = 1 b = 2 c = 3 args = (4,) kw = {'x': 99}
     
      * 递归参数 fact(n) 自己调用自己，如果没有遇到退出的条件，会一直自己调用自己.
      
      ```python
      
      def fact(n):
        if n == 1:
          return 1
        return n * fact(n - 1)
        print fact(1)
        print fact(5)
        
      ```
      1
      120
      
      * 高级特性
      
      ```python
      
      L = []
      n = 1
      while n <= 99:
        L.append(n)
        n = n + 2
        
      ```
      [1,3,5,7,...99]
      
      * 切片 取N个元素
      
      ```python
      L = ['Michael', 'Sarah', 'Tracy', 'Bob', 'Jack']
      r = []
      n = 3
      for i in range(n):
        r.append(L[i])
      print r
      
      print L[0 : 3]
      
      ```
      ['Michael', 'Sarah', 'Tracy']
     
      ['Michael', 'Sarah', 'Tracy']
      
      ```python
      
      L = range(100)
      print L[:10]
      print L[-10:]
      print L[10 : 20]
      print L[: 10 : 2]
      print L[: : 5]
      
      ```
      [0,1,2,3,4,5,6,7,8,9]
      [90,91,92,93,94,95,96,97,98,99]
      [10,,11,12,13,14,15,16,17,18,19]
      [0,2,4,6,8]
      [0,5,10,15,20,25,30,35,40,45,50...95]
      
      * tuple也是一种list，唯一区别tuple不可变.
      
      ```python
      
      print (0,1,2,3,4,5,6)[:3]
      
      ```
      (0,1,2)
      
      * 字符串、Unicode字符串也可以看做是一种list.
      
      ```python
      
      print 'ABCDEFG'[:3]
      
      print 'ABCDEGF'[: : 2]
      
      ```
      'ABC'
      'ACEG'
      
      * 迭代 给list、tuple通过for循环来遍历这个list、tuple，（iteration） for...in
      
      ```python
      
      d = {'a': 1, 'b': 2, 'c': 3}
      for key in d:
        print key
        
     ```
     a
     b
     c
     
     * 判断对象是否可以迭代 collections模块的iterable
     
     ```python
     
     from collections import Iterable
     
     print isinstance('abc', Iterable) #str是否可迭代
     
     ```
     True
     
     ```python
     
     print isinstance([1,2,3], Iterable) #list是否可迭代
     
     ```
     Ture
     
     print isinstance(123, Iterable) #整数是否可迭代
     
     False
  
     * list变成索引-元素对 enumerate
     
     ```python
     
     for i, value in enumerate(['A', 'B', 'C']):
      print i, value
      
     ```
     0 A
     1 B
     2 c
     
     ```python
     
     for x, y in [(1, 1), (2, 4), (3, 9)]:
      print x, y
      
     ```
     1 1
     2 4
     3 9
    
    * 任何可迭代对象都可以作用于for循环，包括我们自定义的数据类型，只要符合迭代条件，就可以使用for循环 
    
    * 列表生成器 List Comprehensions
    
     ```python
     
     print range(1, 11)
     
     ```
     [1,2,3,4,5,6,7,8,9,10]
     
     ```python
     
     L = []
     for x in range(1, 11):
      L.append(x * x)
     print L
     
     ```
     [1,4,9,16,25,36,49,64,81,100]
     
     ```python
     
     print [x * x for x in range(1, 11)]
     
     ```
     [1,4,9,16,25,36,49,64,81,100]
     
     ```python
     
     print [x * x for x in range(1, 11) if x % 2 == 0]
     
     ```
     [4, 16, 36, 64, 100]
     
     ```python
     
     print [m = n for m in 'ABC' for n in 'XZY']
     
     ```
     ['AX', 'AY', 'AZ', 'BX', 'BY', 'BZ', 'CX', 'CY', 'CZ']
     
     * for循环可以同时使用两个甚至多个变量
     
     ```python
     
     d = {'x': 'A', 'y': 'B', 'z': 'C'}
     for k, v in d.iteritems():
      print k, '=', v
      
      ```
      y = B
      x = A
      z = C
      
      ```python
      
      d = {'x': 'A', 'y': 'B', 'z': 'C'}
      [k  + '=', v for k, v in d.iteritems()]
      
      ```
      ['y=B', 'x=A', 'z=C']
      
      * 把一个list中所有的字符串变成小写
      
      ```python
      
      L = ['hello', 'world', 'IBM', 'Apple']
      print [s.lower() for s in L]
      
      ```
      ['hello', 'world', 'ibm', 'apple']
      
      
      * 运用列表生成式，可以快速生成list，可以通过一个list推导出另一个list
      
      *  判断一个变量是不是字符串 内建函数isinstance
      
      ```python
      
      x = 'abc'
      y = 123
      print isinstance(x, str)
      print isinstance(y, str)
      
      ```
      True
      False
      
      ```python
      
      L = ['Hello', 'World', 18, 'Apple', None]
      print [s.lower() if isinstance(s, str) else s for s in L]
      
      ```
      ['hello', 'world', 18, 'apple', None]
      
      * 生成器 一边循环一边计算的机制，称为生成器（Generator）
      
      ```python
      
      L = [x * x for x in range(10)]
      print L
      g = (x * x for x in range(10))
      print g
      
      ```
      [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
      <generator object <genexpr> at 0x104feab40>

      * 创建L和g的区别仅在于最外层的[]和()，L是一个list，而g是一个generator
       +
      * 斐波拉契数列 （Fibonacci） 1，1，2，3，5，8，13，21，34...
      
      ```python
      
      def fib(max):
        n, a, b = 0, 0, 1
        while n < max:
          print b
          a, b = b, a + b
          n = n + 1
        print fib(6)
      
      ```
      1
      1
      2
      3
      5
      8
      
      * yield
      
      ```python
      
      def fib(max):
        n, a, b = 0, 0, 1
        while n < max:
         yield b
          a, b = b, a + b
          n = n + 1
        print fib(6)
        
      ```
      <generator object fib at 0x104feaaa0>
      
      * 函数式编程 Functional Prongramming
      
      * 高阶函数 Higher-order function
      
      * 变量可以指向函数
      
      ```python
      
      print abs(-10)
      print abs
      
      ```
      10
      <built-in function abs>
      
      * abs(-10)是函数调用，而abs是函数本身
      
      ```python
      
      x = abs(-10)
      print x
      f = abs
      f
      
      ```
      10
      <built-in function abs>
      
      * 变量指向函数
      
      ```python
      
      f = abs
      print f(-10)
      
      ```
      10
      
      * 函数名字也是变量
      
      ```python
      
      abs = 10
      print abs(-10)
      
      ```
      报错
      
      * 传入函数 既然变量可以指向函数，函数的参数能接收变量，那么一个函数就可以接收另一个函数作为参数，这种函数就称之为高阶函数
      
      ```python
      
      def add(x, y, f):
        return f(x) + f(y)
      print add(-5, 6, abs)
      
      ```
      11
      
      * map map()函数接收两个参数，一个是函数，一个是序列，map将传入的函数依次作用到序列的每个元素，并把结果作为新的list返回
      
        ```python
        
        def f(x):
          return x * x
        print map(f, [1,2,3,4,5,6,7,8,9])
        
        ```
        [1,4,9,16,25,36,49,64,81]
        
        
        map()传入的第一个参数是f，即函数对象本身
        
        ```python
        
        print map(str, [1,2,3,4,5,6,7,8,9])
        
        ```
        ['1', '2', '3', '4',...'9']
        
        * reduce 把一个函数作用在一个序列[x1, x2, x3...]上，这个函数必须接收两个参数，reduce把结果继续和序列的下一个元素做累积计算
        
        ```python
        
        def add(x, y):
          return x + y
        print reduce(add, [1,3,5,7,9])
        
        ```
        25
        
        ```python
        
        def fn(x, y):
          return x * 10 + y
        print reduce(fn, [1,3,5,7,9])
        
        ```
        13579
        
        ```python
        
        def fx(x, y) :
          return x * 10 + y
          
        def char2num(s):
          return {'0': 0, '1': 1, '2': 2, '3': 3, '4': 4, '5': 5, '6': 6, '7': 7, '8': 8, '9': 9}[s]
        print(fn, map(char2num, '13579')) 
        
        ```
        13579

          
        
        
        
        
        
        
          
          
      
      
      
      
      
      
      
      
   
     
    
    
      
      
      
      
      
      
      
      
    
      
      
     
      
      
      
      
      
      
      
      
      
      
      
       
      
      
       
       
       
       
       
       
       
      
      
      
      
      
      
      
      
      
    
      
      
      
      
      


      
      
        
        
           
      
       
 
          
        
     
     
    
    
    
    
    
    
    
    
    
