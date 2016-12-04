# Pthon笔记

##容器篇
   * 列表list = [1,2,3.....]
  
      ```python

         zhiyi = ['a','b','c','d']
      ```
    
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

          * items()

          ```python 

             for k, v in items():
              print k, v

          ```

          * iteritems()

          ```python

            for k,  v in L.iteritems():
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
     
      * 递归参数 
     
      
      
      
      
      
      
      
      
      
      
      
       
      
      
       
       
       
       
       
       
       
      
      
      
      
      
      
      
      
      
    
      
      
      
      
      


      
      
        
        
           
      
       
 
          
        
     
     
    
    
    
    
    
    
    
    
    
