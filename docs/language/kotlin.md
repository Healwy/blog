# kotlin

## @JvmOverloads 注解
@JvmOverloads注解的作用就是：在有默认参数值的方法中使用@JvmOverloads注解，则Kotlin就会暴露多个重载方法。
通常用于继承时构造函数的重载, 这样就不用每个构造函数都重写一下了。
```
class MyLayout @JvmOverloads
constructor(context: Context, attributeSet: AttributeSet? = null, defStyleAttr: Int = 0) :
    RelativeLayout(context, attributeSet, defStyleAttr) {

}
```
相当Java中的：
```
public class MyLayout extends RelativeLayout {

    public MyLayout(Context context) {
        this(context, null);
    }

    public MyLayout(Context context, AttributeSet attrs) {
        this(context, attrs, 0);
    }

    public MyLayout(Context context, AttributeSet attrs, int defStyleAttr) {
        super(context, attrs, defStyleAttr);
    }
}
```

注：该注解也可用在构造方法和静态方法。
