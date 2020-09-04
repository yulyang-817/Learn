## config
    jupyter
安装包工具

    pip3 ---mac 
    pip ----win
## case1
```python
import matplotlib.pyplot as plt
import math

aum=1
#数组
rec=[]
#循环
days=range(1,365)
for day in days:
    rec.append(aum)
#画图
plt.plot(days,rec)
plt.title("name")
```
## 数据类型
    字符串: ''或""
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
      
  


