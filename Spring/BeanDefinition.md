## BeanDeffinition 结构
class
scope
autowireMode  注入模式  有五种  一种废弃了  0  包扫描（默认模式）
lazyInit
abstractFlag
dependsOn
constructArgumentValues

## 加载类定义
@Bean @ComponentScan -----BeanDefinition列表  装入BeanDefinitionMap里

## BeanFactory循环到Map里取出初始化

## BeanFactoryPostProssor 在类没有初始化的时候修改   提供给用户自己处理的机会   

## 怎么修改呢？
修改class
修改注入模式
修改构造函数参数


##  Bean初始化后 BeanPostProcessor  修改
