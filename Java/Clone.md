需要实现Clonable 接口  可克隆  

clone()  基本数据类型+String   可以克隆  

如果是实体对象属性  克隆后  指向的是一个对象   修改一个  会影响另一个

可以在实体对象属性 事项Clonable

然后在构造函数里 调用这个实体对象的clone  实现深拷贝
```java
public class Test implements Cloneable {

    public  int a  = 1;
    public  T b = new T(1);

    public Test clone() throws CloneNotSupportedException {
        Test t = (Test) super.clone();
        T tt =  (T)this.b.clone();
        t.b = tt;
        return t;
    }



    public static void main(String[] args) throws CloneNotSupportedException {
        Test test1 = new Test();
        Test test2 = (Test) test1.clone();
        test2.a = 5;
        test2.b.b = 222;
        System.out.println(test1 ==  test2);
        System.out.println(test1.a + " --"  + test2.a);
        System.out.println(test1.b.b + " --"  + test2.b.b);

    }
}
```
