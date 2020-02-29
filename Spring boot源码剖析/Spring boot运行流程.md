

## 1.判断是否Web环境
## 2.load spring.factories ApplicationContextInitializer
## 3.load spring.factories ApplicationListener
## 4.判断main方法所在的类
## 5.execute run()
## 6.设置java.awt.headless系统变量
## 7.load spring.factories SpringApplicationRunListener
## 8.执行所有的SpringApplicationRunListener的started方法
## 9.初始化AppliationArguments对象 创建对象
## 10.执行SpringApplicationRunListener的enviromentPrepared()
## 11.如果不是web 环境，但是是web的enviroment, 则是吧这个web的enviroment转化为标准的enviroment
## 12.打印banner
## 13.初始化ApplicationConext 如果是web，则初始化AnnotationConfigEmbeddedWebApplicationAContext,否则实例化AnnotationConfigApplicationContext
## 14.如果beanNameGenerator不为空则注入到context里
## 15.回调所有的ApplicationContextInitializer方法
## 17. 执行所有的SpringApplicationRUnListener的contextPrepared方法
## 18. 一次在Spring容器中注入ApplicationArguments,Banner
## 19.加载所有的源到context
## 20.执行所有的SpringApplicationRunListener的contextLoaded方法
## 21. 执行context的refresh方法，并且调用context的registerShutdownHook方法
## 22. 回调，获取容器中所有的ApplicationRunner， commandlinerunner 排序依次调用
## 23.执行SpringApplicationRunListener的finished方法



