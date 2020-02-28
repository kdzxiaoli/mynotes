# 三种注入ApplicationContext的方法  
1.@Autowired  
ApplicationContext context ;  
context.getClass()  

2. implements ApplicationContextAware  
   //判断是否ApplicationContextAware的子类  是的话在初始化后注入ApplicationContext 
   setApplicationContext(ApplicationContext context) {  
       this.context = context;  
   }  
   
 3.通过构造函数 局限性为多参数构造函数  就报错  找默认构造函数  所以只能有一个构造函数  如果有多个  需要有默认构造函数  这种情况下就达不到效果  
 public Car(ApplicationContext context) {  
     this.context = context;  
 }  
 
 # BeanPostProcessor 每个类初始化后执行
 
 有两个方法  第一个方法表示在依赖属性设置好后执行   第二个是在初始化完成后执行   可以实现该类处理自己的业务逻辑  
 
 #  BeanPostFactoryProcessor 
 spring 容器初始化后执行
 # BeanDefinitionRegistryPostProcessor
 BeanDefinitionBuilder builder = BeanDefinitionBuilder(Car.class);
