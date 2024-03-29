# rule-engine-gradle（规则引擎-gradle版）
# 基于 jdk8  drools7.11.0  gradle
## 背景 
在目前的很多行业应用中，如银行、保险、互联网金融等领域，存在着大量的业务规则，这些业务规则有如下特点：  
1、业务规程数量繁多、非常复杂、且规则处于不断的更新变化中；  
2、现有系统的做法是将业务规则绑定在程序代码中。  

### 存在问题：
1、当业务规则变更是，对应的代码也得更改，即使每次小的变更也需要经历开发、测试、验证上线等过程，变更成本比较大；  
2、长时间系统变得越来越难以维护；  
3、系统僵化，新需求插入困难；  
4、新需求上线周期较长。  

规则引擎是一种嵌套在应用程序中的组件应用，实现了将业务规则从程序代码中分离出来。规则引擎使用特定的语法编写业务规则。  
规则引擎可以接受数据输入、解释业务规则、并根据业务规则做出对应的决策。
 

### 引入规则引擎带来的好处
1、实现业务逻辑和业务规则的分离，实现业务规则的集中管理；  
2、可以动态修改业务规则，从而快速响应需求变更；  
3、业务分析人员可以参与编辑、维护系统的业务规则。  


# 代码实现说明 
具体规则存放在数据库中，执行的时候根据规则编码，提取规则，加载到规则引擎中计算  
代码模拟数据库中的读取，实际规则放在drl规则文件   
可以灵活内嵌到项目代码中，即插即用，无需配置。代码下载后，通过junit单元测试类可以模拟运行  
具体功能提供如下接口：  
1、验证规则有效性--提供验证规则有效性接口  
2、单事实无参规则--提供执行单事实无参规则接口  
3、单事实带参规则--提供执行单事实带参规则接口  
4、事实集合无参规则--提供执行事实集合无参规则接口  
5、事实集合带参规则--提供执行事实集合带参规则接口  



