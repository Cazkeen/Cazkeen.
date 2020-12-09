

```python
def __init__(self,name,age,weight,tall):    # 初始化函数
    self.name = name
    self.age = int(age)
    self.weight = int(weight)
    self.tall = float(tall)

def say(self):
    print("{n},的BMI是,{p}".format(n=self.name,p=self.weight/(self.tall*self.tall)))
    p=self.weight/(self.tall*self.tall)    # 计算BMI值
    if p<18.5:                             # 判断BMI标准
        print("偏瘦")
    elif p<24:
        print("正常")
    elif p<30:
        print("偏胖")
    else :
        print("肥胖")
name=input(“姓名：”) # 输入个人资料（姓名，年龄，体重，身高）
age=input(“年龄：”)
weight=input(“体重：”)
tall=input(“身高：”)

bmi1=BMI(name,age,weight,tall) # 实例化

bmi1.say() # 调用，输出
```
