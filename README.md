# 应用逻辑简介

app 中，开发人员常常将业务处理内容封装成方法，方便开发维护和重复使用。这些被封装的方法，里面的代码内容块，是具体业务数据处理逻辑。不同的逻辑内容，体现了不同功能业务需求和交互设计需求。

iBiz 前端模型，将此类具有公共业务需求的数据处理过程对象化，一同构成了应用逻辑的全部内容。

## 逻辑内容

在 iBiz 前端模型中，逻辑的构成是一个中性的结构模型。通过业务配置，将逻辑放入载体（视图、部件）中后，逻辑业务需求才通过结构代码块得到表现，这些代码块包含了业务逻辑模型全部内容。

应用逻辑主要模型对象构成如下：

| 模型名称 | 详情                                                         | 备注 |
| -------- | ------------------------------------------------------------ | ---- |
| 界面逻辑 | [ IPSViewLogic](https://modelapi.ibizlab.cn/#/net/ibizsys/model/view/IPSViewLogic) |      |
| 界面行为 | [ IPSUIAction](https://modelapi.ibizlab.cn/#/net/ibizsys/model/view/IPSUIAction) |      |
| 界面引擎 | [IPSUIEngine](https://modelapi.ibizlab.cn/#/net/ibizsys/model/res/IPSUIEngine) |      |

### 事件

> 注：从模型组成来讲，逻辑事件属于逻辑的一部分，此处将它单独列为一个小节，是为了方便理解。

事件是逻辑执行的入口，事件的触发点绑定在部件上，部件分发事件

#### 事件起点

事件起点主要提供两个功能：其一，分发事件到部件事件中；其二，执行调用引擎内置逻辑。

#### 部件事件

部件事件主要功能是从被指定的容器对象中获取数据，交给后续界面行为使用，两者的区别在于是在当前操作的 [控件容器]( https://modelapi.ibizlab.cn/#/net/ibizsys/model/control/IPSControlContainer ) 是否与 [部件数据容器]( https://modelapi.ibizlab.cn/#/net/ibizsys/model/control/IPSControlXDataContainer )  为同一个对象。

如果两个对象一致，则直接从该部件事件载体是部件，直接从部件获取数据；如果两个对象不一致，则该部件事件载体是视图，视图需要从对应的部件中获取数据。

### 行为



### 引擎



## 逻辑结构



## 触发流程

{% mermaid %}
graph TD;
  A-->B;
  A-->C;
  B-->D;
  C-->D;
{% endmermaid %}