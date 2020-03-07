魔法内  
绕过虚拟机 直接操作内存

要使用它  必须是bootstrapc lassloader 加载  才能使用   


可以用反射获取
```java
public static Unsafe relfectGetUnsafe() {
	

	try {

	     Field filed = Unsafe.class.getDeclaredField(name: "theUnsafe");
	     field.setAccessible(true);
	     return (Unsafe)field.get(null);
	} catch(Exception e) {
	     e.printStackTrace();
	}
	return null;
}
```
