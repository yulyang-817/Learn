## config
    jupyter
安装包工具

    pip3 ---mac 
    pip ----win
   
## 数据类型
### 字符串: ''或""
      name="my name is yyl1"
    字符串切片:
      name[0:2] 'my' 不包括最右边字符
      name[:4] 'my n'
      name[4:] 'ame is yyl1' 包含最左边字符
      name[-15:] 'my name is yyl1' 从右向左，从-1开始
      
```python
  #字符串方法：
    str.lower()
    str.upper()
    #使用将str分割，默认是空格
    str.split(sep) 
    #按空格分割
    str.split(' ')
    str.replace(old,new)
    #填充
    str.format()
    #自动填充
    template="{name},你的工资是{salary}元：以下是你的工资详情"
    print（template.format(name='张三'，salary='2310'));
    print（template.format(name='2'，salary='230'));
    print（template.format(name='3'，salary='2310'));
    
    #字符串拼接
    join()
    '-'.join(re.findall(pattern,test))  ---->'1950-3'
 ```  
 
```python
        #转义字符
        print('I'm "ok"!') 出错
        print('I\'m \"OK\"!')
        #\t 占2字节
        #\\ 表示字符\ 1字节
        #\n 换行
        print('\\\t\\'） 结果为\     \
        print(r'\\\t\\') 结果为\\\t\\
```
### 列表list，元组tuple
```python
import matplotlib.pyplot as plt
import math

aum=1

#列表
rec=[]
#元组
rec=()
#循环
days=range(1,365)
for day in days:
    rec.append(aum) #添加一个元素
    rec.extend([aum,aum1]) #添加一个列表
    rec.count(aum) #统计列表中aum的个数
    
#集合 {}:实现去重,但没有顺序
#集合方法 add(elm)
rec_set=set(rec)
rec_set.add(elm)
#注意：集合不能切片，不能用rec_set[3]

#画图
plt.plot(days,rec)
plt.title("name")
```      
  
### 字典
```python
#key-value组成，可以存列表，字符串以及嵌套字典

david = dict()
david['age']=23
print(david)
#{age:23}
#字典嵌套字典
infos={david：{'age':23,'gender':'Male'},
       Henry: {'age':25,'gender':'Female'}
      }
#key: david 
#value:'age':23,'gender':'Male'

#方法
#返回所有item
.items() 
    #把 .items()转化为列表,可用切片
    list(david.items())[0]
#返回所有关键词
keys()
#返回所有值
values()
#通过key获取关键信息
get(age)
david[age]
#23
#若关键词不在字典中，返回None
```
### 布尔值和None
    True,False,None（特殊的空值）
    in, not in ,and ,or , not False
### 逻辑语句 if&for&tryexcept
```python
    if else
    
    for i in range(1,n):
        do something
    #字典
    for name,info in infos.items():
    #key值
        print(name);
    #value值
        print(name,info)
    
    try-except
    #遇到0会终止
    for x in [1,2,0,2,1]:
        print(10/x)
    #跳过，不终止
    for x in [1,2,0,2,1]:
    try:
        print(10/x)
    except:
        pass
```

### 练习1：能力为1，每天比前一天多0.01,1年以后能力为多少

    安装包的方法
    pip3 install packagename
    
```python
import matplotlib.pyplot as plt
import math
%matplotlib inline

ab=1
scale=1.01
rec=[]
days=range(1,366)
for day in days:
    ab=ab*scale
    rec.append(ab)
plt.plot(days,rec)
plt.title("Be better everyday!")
```
### 练习2：打印99乘法表
```python
for row in range(1,10):
    #print(row)
    for col in range(1,row+1)
    #用字符串方法，打印公式
        formula='{col}*{row}={res}'.format(col=col,row=row,res=col*row)
    #打印制表符
        print(formula,end='\t')
    #print('\n'):print()默认自带一个\n
    print()
```    
### 列表推导式
```python
    #{x*x|0<x<X}   
    [x*x for x in X]
    
    #有条件情况
    [x*x for x in X if x>5]
    
    #转小写
    [w.lower() for w in words]
    
    #计算列表数据的单词词频
    words=set(mydefine_words)
    [(w,mydefine_words.count(w)) for w in words]
    
    #对字典拼接
    d={'x':'A','y':'B','z','C'}
    #d.items()
    [i[0]+i[1] for i in d.items()]
    #输出['xA','yB','zC']
```

### 函数
```python
    def solution(arg1,arg2)
        return 
    hello(arg1=x,arg2=y)
    hello(arg2=y,arg1=x)
```   
### 常用内置函数
```python
#数字相关
abs(a)
max(lst),min(lst)
sum(lst)#数字求和
sorted(lst,reverse) #对lst排序,参数reverse为布尔值控制升降序
range(start,end,step)

#类型转换
int(string)
float(int/str)
list(iterable) #list(range(1,5)) ----->[1,2,3,4]
emumerate(lst) #给列表中每个元素分配一个索引值 names = ['张三', '李四', '王五'] list(enumerate(names)) ----->[(0, '张三'), (1, '李四'), (2, '王五')]
tuple(lst)  #tuple([1,2,3]) ---->(1,2,3)
set(lst) #list变集合

#功能函数
eval(expression) #执行一个字符串表达式 eval('1+1') 输出2
zip(lst1,lst2....) #lst1和lst2合并，需要list处理一下zip对象 list(zip([1,2,3],[4,5,6])) ---->[(1,4),(2,5),(3,6)]
type(a) #查看数据类型
help(函数名) #查看函数
map(func,lst) #映射运算 func函数
f=open(file,mode,encoding=) #file:相对路径 mode:r和a+ encoding:utf-8和gbk
f.read()
f.write()
f.close()
```
### 内置库-pathlib库
    import pathlib 
    #当前代码所在文件夹的相对路径
    pathlib.Path()
    
    pathlib.Path()属性方法
    #获取当前代码绝对路径
    cwd()
    Path().cwd()
    
    #将grandpa,father,file加入某路径中
    Path().cwd().joinpath(grandpa,father,....file)
    
    #返回某路径下的文件(夹)目录
    Path().cwd().iterdir()
    
    #查找某路径内满足pattern的所有文件路径 
    glob()
    list(Path().cwd().joinpath('data').glob('*.*'))
    
    #判断某路径是否为一个文件。返回布尔值：
    fpath=Path(...)
    fpath.is_file()
    is_dir()
    #路径是否存在
    exists()
    
    #创建某路径
    path = Path().cwd().joinpath('data', 'stocks', '800000')
    path.mkdir(parents=True, exist_ok=True)

### 内置库-数据存储csv库
    #新建csv文件
    import csv
    path='data/test.csv'
    csvf=open(path,'a+',encoding='utf-8',newline='')
    
    #定义字段名，并初始化csv文件为writer
    fieldnames=['name','age']
    writer=csv.DictWriter(csvf,fieldnames=filednames)
    writer.writeheader()
    
    #将待存储数据整理为字典格式
    test_data={'name':'David','age':25}
    
    #用writer往csv中存储数据
    writer.writerow(test_data)
   
    #关闭csv文件
    csvf.close()
    
### 内置库-正则表达式re库
正则表达式主要用于数据清洗，比如从脏乱差的文本中抽取出自己需要的信息。常见于爬虫和文本分析。
    import re
    
    re.findall(pattern,string)
    re.split(pattern,string) #分割  pattern='.|,' 按上述分割
    re.sub(pattern,repl,string) #替换 
    #pattern:正则表达式
    
    1.搜索引擎检索到自己需要的正则表达式（可百度）
    
    2.最简单最好用表达式(.*?) 左右两侧必须有字符，否则匹配失败
    import re
    pattern='我叫(.*?),来自(.*?),今年(.*?)岁'
    intros=['sfdsf我叫张三，来自山东，今年25岁'，
            '213213我叫李四，来自山西，今年28岁']
    for intro in intros:
        info=re.findall(pattern,intro)
        print(info)
        
    3.在[正则表达式测试网站](http://c.runoob.com/front-end/854) 验证自己的正则表达式
      注意:去除^开始符和$结束符
        
 ### python常见错误
     1. 忘记写冒号
     在 if、elif、else、for、while、def语句后面忘记添加 :
     
     2. 错误的缩进
     Python用缩进区分代码块，不要轻易缩进
     if等语句下要缩进
     
     3. 不同数据类型的拼接
     同种数据类型 字符串/列表/元组 支持拼接
     字典/集合:set不支持拼接
     'I have {} eggs.'.format(12)
     
     4. 使用了python中的关键词
     如try、except、def、class、object、None、True、False等
     
     5.编码错误
     一般情况，添加pram recoding='gbk/utf-8'
     如果仍然不行，用以下方法
        import chardet
        #读取为二进制数据
        binary_data = open('data/twitter_sentiment.csv', 'rb').read()

        #传给chardet.detect，稍等片刻
        chardet.detect(binary_data)
        {'encoding': 'Windows-1252', 'confidence': 0.7291192008535122, 'language': ''}
        
        #用找到的最大可能的编码方式编码
        import pandas as pd
        df = pd.read_csv('data/twitter_sentiment.csv', encoding='Windows-1252')
        df.head()
     
    6. 路径字符串写法
    Mac&Win 推荐使用 / 写法
    \n,\t,\d
     
    
    
