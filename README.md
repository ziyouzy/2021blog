# 2021blog

### 2021学习笔记，记录于Wiki标签，有没有整体移动，保存到本地或拥有搜索引擎功能的博客的好方法

**2021年2月14日09点31分:**  
调用zadapter库的adapter的map实体时要注意学习go-logger的这段代码：  

    logFun, ok := adapters[adapterName]
	      if !ok {
		        printError("logger: adapter " + adapterName + "is nil!")
	      }
    adapterLog := logFun()
    
先取出预加载功能函数，然后通过()拿到对应适配器的实体对象(结构类所实现的接口包括了所有底层数据的功能需求)
