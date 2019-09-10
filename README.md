### 服务端

---

#### 背包模块

##### __init__.py

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

用于定义背包对象

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

---

#### 组件模块

##### __init__.py

用于定义组件基类

```python
# 组件基类
class CBaseComponent(object):
    def __init__(self,parentObj):
        self.parent=parentObj   # 保持父节点
        # todo...
        
    # 消息函数
    def OnRecMsg():
        pass
        
    # 其他逻辑...
```

##### defines.py

用于定义枚举类型

```python
SUB_HP_MSG = 1  # 掉血事件消息
#todo...
```

##### XXXComponent1.py 

用于定义其他类型的组件

```python
# 某组件
class XXXComponent1(object):
    def __init__(self,parentObj):
        self.parent=parentObj   # 保持父节点
        # todo...
        
    # 存储到数据库
    def SaveToDataBases():
        pass
        
    # 加载到程序中
    def LoadToProgrammer():
        pass
        
    # 消息函数
    def OnRecMsg():
        pass
        
    # 其他逻辑...
        
```

##### XXXComponent2.py 

用于定义其他类型的组件

```python
# 某组件
class XXXComponent2(object):
    def __init__(self,parentObj):
        self.parent=parentObj   # 保持父节点
        # todo...
        
    # 存储到数据库
    def SaveToDataBases():
        pass
        
    # 加载到程序中
    def LoadToProgrammer():
        pass
        
    # 消息函数
    def OnRecMsg():
        pass
        
    # 其他逻辑...
   
```

---

#### 怪物池模块

##### objects.py 

用于定义怪物池对象

```python
# 怪物池
class MyEnemyPool(object):
    def __init__(self,playerId):
        # todo...
        
    def CreateEnemyList():
        pass

    # 其他逻辑...
```

##### genobj

用于存放怪物池对象

##### __init__.py

```python

from myenemypool.genobj import mep1001
from myenemypool.genobj import mep1002

if g_myEnemyPool not  in golbals():
    g_myEnemyPool={}
    
g_myEnemyPool[1001]=mep1001
g_myEnemyPool[1002]=mep1002
# todo...
```

怪物池的生成对象存放字典

```python
# 怪物池
class MyEnemyPool(object):
    def __init__(self,playerId):
        # todo...
        
    def CreateEnemyList():
        pass

    # 其他逻辑...
```

##### mep1001.py

```python
# 怪物池
class MyEnemyPool(object):
    def __init__(self,playerId):
        # todo...
        
    def CreateEnemyList():
        pass

    # 其他逻辑...
```

##### mep1002.py

```python
# 怪物池
class MyEnemyPool(object):
    def __init__(self,playerId):
        # todo...
        
    def CreateEnemyList():
        pass

    # 其他逻辑...
```


---

#### 事件模块

##### __init__.py

用于定义全局字典，存储对象引用

```python
if g_myEventPro not  in golbals():
    g_myEventPro={}

# 增加事件概率
def AddEventPro(playerId):
    pass
    
# 减少概率
def SubEventPro(playerId):
    pass
    
# 事件概率
def GetEventPro(playerId):
    pass
```

##### defines.py

用于定义枚举类型

```python
GET_MONEY = 1 #获得金币
#todo...
```

##### net.py

用于定义通信模块接口及实现

```python
# 客户端到服务端
# ClientToServer:

def FightEvent(playerId):
    pass

# todo...

# 服务端到客户端
# ServerToClient:
def EventOver(playerId):
    pass
    
#todo...
```

##### effect.py

用于定义事件效果及实现

```python
def Effect1():
    pass
    
def Effect2():
    pass
    
g_myEventEfDict={
    GET_MONEY:Effect1
    # ...
}

#todo...
```


##### objects.py 

用于定义事件对象

```python
# 事件
class MyEvent(object):
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

##### genobj

用于存放事件对象

##### __init__.py

```python

from myevent.genobj import me2001
from myevent.genobj import me2002

if g_myEvent not  in golbals():
    g_myEvent={}
    
g_myEvent[2001]=me2001
g_myEvent[2002]=me2002
# todo...
```

事件对象存放字典

```python
class MyEvent(object):
    def __init__(self,playerId):
        # todo...
        
    # 其他逻辑...
```

##### me2001.py

```python
class MyEvent(object):
    def __init__(self,playerId):
        # todo...
        
    # 其他逻辑...
```

##### me2002.py

```python
class MyEvent(object):
    def __init__(self,playerId):
        # todo...
        
    # 其他逻辑...
```


---

#### 战斗模块

##### __init__.py

用于定义全局字典，存储对象引用

##### defines.py

用于定义枚举类型

##### net.py

用于定义通信模块接口及实现

##### fightmanager.py

用于管理战斗中的数据、初始化、对外保留基本操作

```python
class FightData():
    pass
    
    def AddPeople():
        pass
        
    def ChangeLocation():
        pass
        
    def SortBySpeed():
        pass
#todo...
```

##### objects.py 

用于定义战斗对象及战斗逻辑

```python
# 战斗
class MyFight(object):
    def __init__(self,playerId):
        self.Data=FightData()
        # todo...
        
    def UseItem():
        pass
        
    def UseSkill():
        pass
        
    def SetOrder():
        pass
        
    def ExcuteOrder():
        pass
        
    # 其他逻辑...
        
```
---

#### 测试模块

##### __init__.py

用于定义全局字典，存储对象引用

##### defines.py

用于定义枚举类型

##### net.py

用于定义通信模块接口及实现

##### testmodel

测试模块

##### testfight.py

##### testbag.py 

##### testskill.py

##### testitem.py 

---

#### 新手引导

##### __init__.py

用于定义全局字典，存储对象引用

##### defines.py

用于定义枚举类型

##### net.py

用于定义通信模块接口及实现

---

#### 心跳系统

##### __init__.py

暂无作用

##### defines.py

用于定义枚举类型

##### net.py

用于定义通信模块接口及实现

---

#### 物品系统

##### 道具

##### __init__.py

用于定义全局字典，存储对象引用

##### defines.py

用于定义枚举类型

##### net.py

用于定义通信模块接口及实现

##### object.py

定义道具基类


##### effect.py

定义道具效果

---

##### 遗物

##### __init__.py

用于定义全局字典，存储对象引用

##### defines.py

用于定义枚举类型

##### net.py

用于定义通信模块接口及实现

##### object.py

定义遗物基类

##### effect.py

定义遗物效果

---

#### 技能系统

---

#### buff系统

---

#### 玩家系统

---

#### 奖励系统

---

#### 怪物系统

---

#### 队伍系统

---

#### 技能树系统

---

#### 商店系统

---

#### 地图系统

---

#### 定时器系统

---

#### 数据库存储系统

---

#### log日志

---

#### 通讯模块

---

#### 登录模块

---

### 客户端