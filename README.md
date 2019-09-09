### 服务端


---

#### 背包模块

##### __init.py

用于定义全局字典，存储对象引用

```python
if g_myBag not  in golbals():
    g_myBag={}

# 移除某对象
def RemoveObj(playerId):
    pass
    
# 添加某对象
def AddObj(playerId):
    pass
    
# 得到某对象
def GetObj(playerId):
    pass
```

##### defines.py

用于定义枚举类型

```python
MY_BAG_CAPACITY = 1 #背包容量
#todo...
```

##### net.py

用于定义通信模块接口及实现

```python
# 客户端到服务端
# ClientToServer:

def AddItem(playerId,Index):
    pass

# todo...

# 服务端到客户端
# ServerToClient:
def InitBag(playerId):
    pass
    
#todo...
```

##### objects.py 

用于定于背包对象

```python
# 背包
class MyBag(object):
    def __init__(self,playerId):
        self.items=ItemsList()
        # todo...
        
    # 存储到数据库
    def SaveToDataBases():
        pass
        
    # 加载到程序中
    def LoadToProgrammer():
        pass
        
    # 其他逻辑...
        
# 道具栏
class ItemsList(object):
    def __init__(self,playerId):
        # todo...
        
    # 存储到数据库
    def SaveToDataBases():
        pass
        
    # 加载到程序中
    def LoadToProgrammer():
        pass
        
    # 其他逻辑...
```