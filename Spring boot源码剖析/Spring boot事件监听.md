# 自定义事件
##  inherit from ApplicationEvent
##  implement ApplicationListener
SpringbootApplication.addListener or add @Component  or context.listener.classes property configration ref DelegatingApplicationContextListener
or
def a @Component MyEventHandler -> @EventListener event(Object event) //all event listener ref EventListenerMethodProcessor
##  Publish event
context.pushlishEvent()




