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
      
        
        
           
      
       
 
          
        
     
     
    
    
    
    
    
    
    
    
    
