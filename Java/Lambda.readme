函数接口只能有一个方法  可以有默认方法 

函数继承的时候  如果方法名有重复的  会提示要用哪个


int i  = IntStream.of(nums).min().getAsInt();

IntStream.of(nums).parallel();
---
new Thread(() -> System.out.println(222);)


方法引用
-> System::out

参数和  使用参数一直  可以用::






非静态方法引用
int app(Dog this, int a) {
	
}

app(111);


jdk 默认会把实力对象传到方法的第一个位置
IntUnaryOperator function = dog::eat;

function.applyasInt();

BiFunction<Dog, Integer, Integer> eatFunc = Dog::eat;

构造函数引用

构造函数  Dog::new

Supplier<Doc> supplier = Dog::new;

supplier.get();


带方法构造函数
Function<String, Dog> function =  Dog::new //参数  返回

要注意下面
List<String> list = new ArrayList<>();
void change(List<String> list) {
	list = null;
}
System.out.println(list); // list is not null please take care



类型推断


IMath lambda = (x, y) -> x + y;


public static Imath test() {
	return (x,y) -> x + y;
}

函数有重载的时候   会有歧义
使用强转解决



变量引用
String str = "";//这里是Final  匿名内部类   只不过jdk8 隐藏了
Consumer<String> consumer = s-> System.out.println("s" + str);
consumer.accept("1211“)


级联表达式  和 柯里化

 

 Function<Integer, Function<Integer, Integer>> = x -> y -> x + y


 柯里化：把多个参数的函数转换为一个参数的函数
 柯里化的目的：函数标准化
 apply.apply.apply
 
















