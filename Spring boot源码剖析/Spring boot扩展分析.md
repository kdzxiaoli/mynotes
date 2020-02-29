 # 1. ApplicationContextInitilizer  
 
spring容器在 refresh之前的回调  允许我们做进一步的初始化    

## implement this class and app.addInitilizer(class)    
## context.initializer.classes=....    
## spring.factories  
org.springframeworkcontext.ApplicationContextInitializer=?  

# 2. CommandLineRunner  
在spring容器执行完了最后一个回调  可以用@Odered控制顺序  
