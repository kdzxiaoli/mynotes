AnnotationConfigApplicationContext context = new AnnotationConfigApplicationContext(MyConfig.class)

BeanFactory 是spring boot的顶级基类 


FactoryBean是spring定义Bean的接口  
可以实现该类  
Example:

class CarFactory implements FactoryBean<Car> {
}


context.getBean("CarFactory") will return Car 
context.getBean(CarFactory.class) or context.getBean("&CarFactory") will return CarFactory 

# Bean的初始化

1.Bean 初始化  可以实现 InitializingBean     销毁 可以实现DisposableBean


2.@Bean(initMethod=?, destroyMethod=?)

3.@PostConstruct  @Destroy  

#依赖注入
@Autowired   @Resource  JSR——250   @Inject  JSR-330

