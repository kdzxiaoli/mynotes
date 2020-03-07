@MapperScan  找到类
扫描包
接口beandefinition
拦截修改

包扫描后 
改所有的接口类为MapperFactoryBean 
它的父类SqlSessionDaoSupport  里面有SqlSessionTemplate  这个类实现了SqlSession
SqlSessionTemplate不能为空  代码里看没有纳入容器   但是是按类型注入的  所以会掉set方法注入  里面就是这个道理

实现了FactoryBean 
通过getObject 方法返回


BeanFactory  io容器

构造函数入参为class
注入模式为按类型  防止 自定义名称随意不报错  容错处理

