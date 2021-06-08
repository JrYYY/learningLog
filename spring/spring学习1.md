## Spring 学习1

 #### 理解 spring ：

spring 主要是工厂代理：

> spring 框架   `@Controller`,`@Repository`,`@Service`   三个注解都携带  `@Component`。spring 通过配置扫描包通过 `@Component` 注解将 class 注入到spring 工厂（控制反转），之后使用对应的类时可以通过访问 spring工厂获取对应的类（依赖注入），注入的可以用的类的方式有： 通过 `@Autowired` 注解注入，通过构造函数注入，setter 方式注入（spring 扫描）； `SpringFactoryUtil.getBean()` 通过 Bean ID 注入直接通过 ID 获取 Bean (`@Component` 注入工厂的时候默认类名为BeanID)。

 * Controller :
```java
@Target({ElementType.TYPE}) //注解使用范围
@Retention(RetentionPolicy.RUNTIME)	//设置注解的生命周期 
@Documented
@Component	//	spring 检测bean 
public @interface Controller {
    String value() default "";
}
```

 * Service :
```java
@Target({ElementType.TYPE})
@Retention(RetentionPolicy.RUNTIME)
@Documented
@Component
public @interface Service {
    String value() default "";
}
```

注入spring 的好处：

 >减少反复需要创建对象（在正常使用过程中都需要 new 来创建这个对象，创建的对象会存到jvm 堆。当一个项目使用量大时，需要反复创建一个对象，这个会导致堆的溢出内存不够；但是通过spring工厂，只需要将service，controller，dao 层的对象都注入到spring 工厂中，在启动项目时将对象保存到spring 工厂，后面每次使用都是在工厂中获取，不需要再进行创建对象）；
