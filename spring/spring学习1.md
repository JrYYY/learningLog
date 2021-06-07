## Spring 学习1

 理解 spring 作用： spring 主要是工厂代理，spring 框架 @Controller，@Repository，@Service 三个注解都携带 @Component。spring 通过配置扫描包通过 @Component 注解将 class 注入到spring 工厂（控制反转），之后使用对应的类时可以通过访问 spring工厂获取对应的类（依赖注入），注入的可以用的类的方式有： 通过 @Autowired 注解注入，通过构造函数注入，setter 方式注入（spring 扫描）； SpringFactoryUtil.getBean() 通过 Bean ID 注入直接通过 ID 获取 Bean (@Component 注入工厂的时候默认类名为BeanID)。
 
 
