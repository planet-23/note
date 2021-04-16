# Spring（弃）

### IOC：控制反转（Bean注入）

 - DAO
 - DAOImpl
 - Service
 - ServiceImpl

~~~ java
public class Student{
    String name;
    //Setter
}
~~~



~~~ xml
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:p="http://www.springframework.org/schema/p"
    xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd">
        
    <bean id="student" class="com.heyong.Student" autowire="byType">
    	<protperty name="name" value="heyong"/>
    </bean>
</beans>
~~~



~~~java
public class test{
    public static void main(String[] args){
        ApplicationContext context=new ClassPathXmlApplicationContext("beans.xml");
        Student student=(Student)context.getBean("student");
        student.getName();
    }
}
~~~



#### DI：依赖注入

​    依赖于Spring容器注入Bean对象的所有属性

	- p命名空间：属性
	- c命名空间：构造函数参数

#### 自动装配

- autowire=""

  ~~~xml
  <?xml version="1.0" encoding="UTF-8"?>
  <beans xmlns="http://www.springframework.org/schema/beans"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:context="http://www.springframework.org/schema/context" 
      xmlns:p="http://www.springframework.org/schema/p"
      xsi:schemaLocation="http://www.springframework.org/schema/beans
          http://www.springframework.org/schema/beans/spring-beans.xsd
                          http://www.springframework.org/schema/context
          http://www.springframework.org/schema/context/spring-context.xsd">
      <context:component-scan base-package=""/>
      <context:annotation-config/>    
      
      <bean id="student" class="com.heyong.Student" autowire="byType">
      	<protperty name="name" value="heyong"/>
      </bean>
  </beans>
  ~~~
~~~
  

#### 注解开发(必须保证AOP包导入)

- @AutoWired
- @Resource
- @Component
- @Scope         // 
  - @Value			//可以用在属性或者set方法上
- @Controller
- @Repository
- @Service
- @Mapper



#### JAVA注入Bean
@Configuration
public class Config{
    @Bean
    public User getUser(){
        return new User();
    }
}
~~~



~~~java
ApplicationContext context=new AnnotationConfigApplicationContext(Config.class)
    User user=(User)context.getBean("getUser");
~~~





### AOP：面向切面编程

#### 静态代理

~~~java
public interface Action{
    public void marry();
} 
~~~



~~~java
public class People implements Action{
    private String name;
    public People(String name){
        this.name=name;
    }
    
    public void marry(){
        System.out.print("结婚");
    }
}
~~~



~~~java
public class Proxy implements Action{
    private People people;
    
    public Proxy(People people){
        this.people=people;
    }
    
    public void marry(){
        System.out.print("筹备");
        this.people.marry();
        System.out.print("收费");
    }
}
~~~



#### 动态代理(代理类动态生成)

- 基于接口的动态代理
- 基于类的动态代理
- 基于字节码的



**Proxy**

**InvocationHandler**

~~~java
public class ProxyInvocationHandler implements InvocationHandler{
    private Rent rent;
    public void setRent(Rent rent){
        this.rent=rent;
    }
    public Object getProxy(){
        return Proxy.newProxyInstance(this.getClass().getClassLoader(),rent.getCalss().getInterfaces,this);
    }
    public Object invoke(Object proxy,Method method,Object[] args)throws Throwable{
        
        //前置操作
        Object result=method.invoke(rent,args);
        //后置操作
        return result;
        
    }
    
}
~~~



~~~java
public class Client{
    public static void main(String[] args){
        Host host=new Host();
        ProxyInvocationHandler phi=new ProxyInvocationHandler();
        phi.setRent(host);
        Rent proxy=(Rent)phi.getProxy();
        proxy.rent();
    }
}
~~~



​	

- **AOP实现**

  1. Spring

  ~~~java
  public class log implements MethodBeforeAdvice{
      public void before(Method method,Object[] args,Object target){
          System.out.print("");
      }
  }
  ~~~

  ~~~xml
  <?xml version="1.0" encoding="UTF-8"?>
  <beans xmlns="http://www.springframework.org/schema/beans"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:context="http://www.springframework.org/schema/aop" 
      xmlns:p="http://www.springframework.org/schema/p"
      xsi:schemaLocation="http://www.springframework.org/schema/beans
          http://www.springframework.org/schema/beans/spring-beans.xsd
                          http://www.springframework.org/schema/aop
          http://www.springframework.org/schema/aop/spring-aop.xsd">
      <!--注册bean-->
      <!--配置AOP-->
      
      <!--切入点-->
      <aop:config>
      	<aop:pointcut id="pointcut" expression="execution(* cpm.kuang.service.User.*(..))"/>
          
          <aop:advisor advice-ref="log" pointcut="pointcut"/>
          </aop:config>
      
  </beans>
  ~~~

  



   2. **第二种**

      ~~~xml
      <aop:config>
      	<aop:aspect ref="log">
          	<aop:pointcut id="point" expression="execution(* com.kuang.service.User.*(..))"/>
              <aop:before method="before" pointcut-ref="point"/>
          </aop:aspect>
      </aop:config>
      
      ~~~

      

   3. 注解实现AOP

      ~~~java
      //先配置xml支持注解
      @Component
      @Aspect
      public class AnnotationPointCut{
          
          @Before("execution(* com.kuang.service.User.*(..))")
          public void before(){
              System.out.print("-------")
          }
          
          @After
          @Around
          //ProceedingJoinPoint jp
          //point.proceed()
      }
      ~~~

      ~~~xml
      <aop:aspectj-autoproxy/>
      ~~~

      



# MySQL

- 关系型数据库
  - MySQL、Oracle、SQL Server、DB2、SQLlite
- 非关系型数据库
  - Redis、Mongodb



**DBMS（数据库管理系统）**

DDL、DML、DQL、DCL



### 数据类型

数值、字符串、时间日期、null



### 字段属性

**Unsigned**

- 无符号整数

**zerofull**

- 0填充

**自增**

**非空**

**默认值**

拓展：

- ID  主键
- 'version'    乐观锁
- is_delete   伪删除
- gmt_create   创建时间
- gmt_update   更新时间



### SQL语法

#### **数据库**

~~~sql
create database [if not exists] stu;	--创建库
drop database [if exists] stu;		--删除库
-- 特殊字符加``
use stu
show databases;

~~~



#### **表**

```sql
--创建表
create table if not exists 'student'(		
	`id` int(4) not null auto_increment primary key comment'主键',
    `name` varchar(100) not null default 'he', 
);

--查看创建表的语句
show create table student		
desc student

--修改表
alter table student rename as stu;
alter table student add age int(11);

alter table student modify age varchar(11);
alter table student change age age1 int(1);

alter table student drop age;

-- 删除表
drop table if exists student;
```



#### **外键约束：不推荐使用**

~~~sql
(
    key `fk_gradeID`(`gradeID`)
    constraint `fk_gradeID`  foreign key(`gradeId`) references `grade`(`gradeID`);

)


alter table student add constraint `fk`  foreign key(`gradeId`) references `grade`(`gradeID`);
~~~



#### **DML**

```sql
-- 添加
insert into 表() values(),();
-- 修改
update 表 set 列="",列="" where 条件
-- 删除
delete from 表 where 条件

-- 清空表
delete from 表		-- 不建议使用，不会重置自动增长
truncate table 表 
```

#### DQL

```sql
select 列 ，列 from 表 where 条件
select 列 as 别名 from 表 as 别名 where 条件
select concat('',列)	from 表 where 条件
select distinct * from userName;


-- 函数
concat()     --字符串连接
version()	--版本
distinct	--去重
```



##### where子句

- **运算符**

| =                     |          |
| --------------------- | -------- |
| <> 或 !=              |          |
| >   <     >=   <=     |          |
| between and           | 闭合区间 |
| and   or   not        |          |
| \|\|       &&      ！ |          |



##### 模糊查询

| is null     |                                             |
| ----------- | ------------------------------------------- |
| is not null |                                             |
| between and |                                             |
| **like**    | **%** ：所有字符     **_**   ：代表一个字符 |
| in          | in(........)                                |



##### 联表查询

| inner join     | 返回查找的所有 |
| -------------- | -------------- |
| **left join**  | 查找右表所有   |
| **right join** | 查找左表所有   |

~~~sql
select s.studentid，gradeId 
from student as s 
inner join grade as g 
on s.studentid=g.studentid 
--- 可以关联多张表
~~~

>where 与join on

- 自连接



##### 分页与排序

- 排序  order by

  - 升序  asc

  - 降序 desc

- 分页 limit

~~~sql
select * from stu limit 5,10;			--起始值，页面大小
~~~

##### 子查询

~~~sql
select * from stu where gradeId=（select gradeId from garde where grade>=80）;
~~~



##### 常用函数

- abs（）     绝对值
- ceiling（）  向上取整
- floor（）   向下取整
- rand（）   随机数0-1
- sign（）  判断符号+-1

[帮助文档](https://www.mysqlzh.com/doc/124.html)

##### 聚合函数（常用）

| count（） | 计数 |
| --------- | ---- |
| sum（）   | 总和 |
| AVG（）   |      |
| max（）   |      |
| min（）   |      |
|           |      |
|           |      |

~~~sql
select count(studentId) from student       	--忽略null值
select count(*) from student 				--
select count(1) from student 
~~~



##### 分组过滤  group by

- 过滤之前用where
- 过滤之后用having



### 事务

- 原则

  ACID：原子性、一致性、隔离性、持久性

~~~sql
set autocommit=0    ---闭事务自动提交
start transaction

commit
rollback
set autocommit=1    ---开启自动提交



savepoint 保存点
rollback to savepoint 保存点
release savepoint 保存点     ---撤销保存点

~~~

- 四大隔离级别



### 索引

- 主键索引（premary key）
- 唯一索引（unique key）
- 常规索引（key/index）
- 全文索引（fullText）



### 数据库引擎

|            | MYISAM               | INNODB   |
| ---------- | -------------------- | -------- |
| 事务支持   | 不支持（最新版支持） | 支持     |
| 数据行锁定 | 不支持               | 支持     |
| 外键约束   | 不支持               | 支持     |
| 全文索引   | 支持                 | 不支持   |
| 表空间大小 | 较小                 | 较大     |
| 优点       | 节约空间、速度快     | 安全性高 |



配置字符集

charset=utf8



### 数据库备份

- mysqldump 命令			source



### JDBC

1. 加载驱动
2. 连接数据库 DriverManager
3. 获取statement对象
4. 执行sql
5. 释放连接



# Mybatis

### 一、导入依赖

```xml
<dependency>
            <groupId>mysql</groupId>
            <artifactId>mysql-connector-java</artifactId>
            <version>8.0.21</version>
        </dependency>

        <!-- https://mvnrepository.com/artifact/org.mybatis/mybatis -->
        <dependency>
            <groupId>org.mybatis</groupId>
            <artifactId>mybatis</artifactId>
            <version>3.5.3</version>
        </dependency>

        <dependency>
            <groupId>junit</groupId>
            <artifactId>junit</artifactId>
            <version>4.13</version>
            <scope>test</scope>
        </dependency>


<build>
        <resources>
            <resource>
                <directory>src/main/java</directory>
                <includes>
                    <include>**/*.xml</include>
                </includes>
                <filtering>true</filtering>
            </resource>
            <resource>
                <directory>src/main/resources</directory>
                <includes>
                    <include>**/*.xml</include>
                </includes>
                <filtering>true</filtering>
            </resource>
        </resources>
    </build>
```



### 二、编写核心配置文件

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE configuration
        PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN"
        "http://mybatis.org/dtd/mybatis-3-config.dtd">
<configuration>
    <properties resource="">
        <property name="" value=""/>
    </properties>
    <!--    <settings>-->
<!--        <setting name="" value=""/>-->
<!--    </settings>-->
    <typeAliases>
        <typeAlias type="com.heyong.blog.Pojo.User" alias="User"/>
        <!--        <package name="com.heyong.blog.Pojo"/>  类名首字小写-->
    </typeAliases>
    
        <environments default="mysql">
            <environment id="mysql">
                <transactionManager type="JDBC"></transactionManager>
                <dataSource type="POOLED">
                    <property name="driver" value="com.mysql.cj.jdbc.Driver" />
                    <property name="url" value="jdbc:mysql://localhost:3306/blog?serverTimezone=Asia/Shanghai"/>
                    <property name="username" value="root"/>
                    <property name="password" value="heyong728350858"/>
                </dataSource>
            </environment>
        </environments>

    <mappers>
        <mapper resource="com/heyong/blog/dao/UserMapper.xml"></mapper>
    </mappers>
</configuration>
```



### 三、编写mapper

~~~xml
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE mapper
        PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN"
        "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.heyong.blog.dao.UserDao">
    <select id="getUser" parameterType="java.lang.Integer" resultType="com.heyong.blog.Pojo.User">
        select * from user;
    </select>
</mapper>

~~~



### 四、获取session

~~~java
package com.heyong.blog.utils;

import org.apache.ibatis.session.SqlSession;
import org.apache.ibatis.session.SqlSessionFactory;
import org.apache.ibatis.io.Resources;
import org.apache.ibatis.session.SqlSessionFactoryBuilder;

import java.io.IOException;
import java.io.InputStream;

public class MybatisUtils {
    private static SqlSessionFactory sqlSessionFactory;

    static {
        String resource= "mybatis-config.xml";
        try {
            InputStream inputStream=Resources.getResourceAsStream(resource);
            sqlSessionFactory =new SqlSessionFactoryBuilder().build(inputStream);
        } catch (IOException e) {
            e.printStackTrace();
        }
    }

    public static SqlSession getSession(){
        return sqlSessionFactory.openSession();
    }
}
//sqlsession.getmapper(UserDao.class)  记得关闭
~~~





### 五、CURD

1. mapper

   ```xml
   parameterType
   resultType
   resultMap
   
   <select id="getUser" parameterType="java.lang.Integer" resultType="com.heyong.blog.Pojo.User">
           select * from user where id=#{id};
       </select>
   
   <select id="getUser" parameterType="com.heyong.blog.Pojo.User" resultType="com.heyong.blog.Pojo.User">
           select * from user where username=#{username};
       </select>
   ```

   >修改需要手动提交
   >
   >map万能



### 六、Log4j

1. 导入包

~~~xml
<!-- https://mvnrepository.com/artifact/log4j/log4j -->
<dependency>
    <groupId>log4j</groupId>
    <artifactId>log4j</artifactId>
    <version>1.2.17</version>
</dependency>

~~~

2. 配置:res路径下

   ~~~properties
   
   ~~~

3. 配置

   ~~~xml
   <settings>
   <setting name="logImpl" value="log4j"/>
   </settings>
   ~~~



### 七、分页

- limit



### 八、注解开发

>绑定接口

~~~xml
<mappers>
        <mapper class="com/heyong/blog/dao/UserMapper"></mapper>
    </mappers>
~~~



~~~java
@Select("")
~~~





### 九、lombok

- 下载插件
- 导入依赖
- 使用



### 十、多对一



### 十一、一对多



### 十二、动态sql

- if
- choose（when、otherwise）     相当于switch
- trim、where、set
- foreach

~~~xml
<if test="">
</if>



~~~





# Spring

### ioc

- ApplicationContext.xml文件：注册bean

  - ~~~xml
    <?xml version="1.0" encoding="UTF-8"?>
    <beans xmlns="http://www.springframework.org/schema/beans"
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd">
        
        <bean id="userService" class="com.heyong.blog.service.Impl.UserServiceImpl">
            <property name="" value=""/>
            <property name="" ref=""/>
            <constructor-arg index="" value=""/>
        </bean>
    </beans>
    ~~~

- pom.xml文件

  - ~~~xml
    <dependency>
                <groupId>org.springframework</groupId>
                <artifactId>spring-context</artifactId>
                <version>5.2.9.RELEASE</version>
           </dependency>
    ~~~

- 获取对象

  - ~~~java
    ApplicationContext context=new ClassPathXmlApplicationContext("beans.xml");
            Student student=(Student)context.getBean("student");
            student.getName();
    ~~~





- 注入方式

  - 基于xml

    - 构造注入
    - set注入

  - 基于注解

    - @Autowired

    - @Resource

    - @Component

    - @Repository

    - @Service

    - @Controller

    - @Value

    - ~~~xml
      <?xml version="1.0" encoding="UTF-8"?>
      <beans xmlns="http://www.springframework.org/schema/beans"
          xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
             xmlns:context="http://www.springframework.org/schema/context" 
          xmlns:p="http://www.springframework.org/schema/p"
          xsi:schemaLocation="http://www.springframework.org/schema/beans
              http://www.springframework.org/schema/beans/spring-beans.xsd
                              http://www.springframework.org/schema/context
              http://www.springframework.org/schema/context/spring-context.xsd">
          <context:component-scan base-package=""/>    组件扫描器
          <context:annotation-config/>    
      </beans>
      ~~~

      

  - 自动注入autowire（只支持引用类型）

    - byName
    - byType

- 放入Spring的类

  - dao、service、controller、工具类

- 不放容器的类

  - 实体类、Servlet、filter、listener等



### 集成mybatis

- mybatis主配置文件

  ~~~xml
  <?xml version="1.0" encoding="UTF-8" ?>
  <!DOCTYPE configuration
          PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN"
          "http://mybatis.org/dtd/mybatis-3-config.dtd">
  <configuration>
      <settings>
       	<setting name="" value=""/>
  	</settings>
      <typeAliases>
          <typeAlias type="com.heyong.blog.Pojo.User" alias="User"/>
          <!--        <package name="com.heyong.blog.Pojo"/>  类名首字小写-->
      </typeAliases>
  
      <mappers>
          <mapper resource="com/heyong/blog/dao/UserMapper.xml"></mapper>
      </mappers>
  </configuration>
  ~~~

  



- 数据源配置

  ~~~xml
  <bean id="dataSource" class="com.alibaba.druid.pool.DruidDataSource" init-method="init" destroy-method="close">
          <property name="password" value=""/>
          <property name="username" value=""/>
          <property name="url" value=""/>
          <property name="driverClassName" value="com"/>
          ............
      </bean>
  ~~~

  

- sqlsessionfactory

  ~~~xml
  <bean id="sqlSessionFactory" class="org.mybatis.spring.SqlSessionFactoryBean">
          <property name="dataSource" ref="dataSource"/>
          <property name="configLocation" value="classpath:mybatis-config.xml"/>
     </bean>
  ~~~

  

- 创建dao

  ~~~xml
  <bean class="org.mybatis.spring.mapper.MapperScannerConfigurer">
          <property name="sqlSessionFactoryBeanName" value="sqlSessionFactory"/>
          <property name="basePackage" value="com.heyong.blog.dao"/>
      </bean>
  ~~~

  



获取方式：getBean（）

- 使用属性配置

  ~~~xml
  <context:property-placeholder location="jdbc.properties"/>
  
  ${属性名}
  ~~~

  



### AOP

- 依赖

  ~~~xml
  	<dependency>
              <groupId>org.springframework</groupId>
              <artifactId>spring-aspects</artifactId>
              <version>5.2.6.RELEASE</version>
          </dependency>
  ~~~

  

- 配置

  ~~~xml
  	<bean id="userService" class="com.heyong.blog.service.Impl.UserServiceImpl"></bean>
      <bean id="myAspect" class="com.heyong.blog.aspects.MyAspect"></bean>
      <aop:aspectj-autoproxy/>
  ~~~

- 配置实现

  ~~~xml
  <aop:config>
  	<aop:aspect ref="log">
      	<aop:pointcut id="point" expression="execution(* com.kuang.service.User.*(..))"/>
          <aop:before method="before" pointcut-ref="point"/>
      </aop:aspect>
  </aop:config>
  ~~~

  

- 注解实现

  ~~~java
  package com.heyong.blog.aspects;
  
  import org.aspectj.lang.annotation.*;
  
  @Aspect
  public class MyAspect {
  
      @Before(value = "execution(* com.heyong.blog.service.*.*(..))")
      public void beforeLog(JoinPoint jp){
          System.out.println("前置日志");
      }
      @Around()
      @After()
      @AfterThrowing()
      @AfterReturning()
      
      @Pointcut(value = "execution(* com.heyong.blog.service.*.*(..))")
      public void mpc(){}
  }
  ~~~

  

### Spring事务

- 依赖

  ~~~xml
  <dependency>
              <groupId>org.springframework</groupId>
              <artifactId>spring-tx</artifactId>
              <version>5.2.9.RELEASE</version>
          </dependency>
          <dependency>
              <groupId>org.springframework</groupId>
              <artifactId>spring-jdbc</artifactId>
              <version>5.2.9.RELEASE</version>
          </dependency>
  ~~~

  

- 利用AOP

  - 注解方式

    ~~~xml
    <!--    事务管理器-->
        <bean id="dataSourceTransactionManager" class="org.springframework.jdbc.datasource.DataSourceTransactionManager">
            <property name="dataSource" ref="dataSource"/>
        </bean>
    <!--开启事务注解驱动-->
        <tx:annotation-driven transaction-manager="dataSourceTransactionManager"/>
    ~~~

    ~~~java
    @Transactional(
                propagation = Propagation.REQUIRED,
                isolation = Isolation.DEFAULT,
                readOnly = false,
                rollbackFor = {Exception.class}
        )
    ~~~

  - 配置文件方式

    ~~~xml
    <!--    事务管理器-->
        <bean id="dataSourceTransactionManager" class="org.springframework.jdbc.datasource.DataSourceTransactionManager">
            <property name="dataSource" ref="dataSource"/>
        </bean>
        
       <tx:advice id="interceptor" transaction-manager="dataSourceTransactionManager">
            <tx:attributes>
                <tx:method name="" isolation="" propagation="" read-only="" rollback-for=""/>  可以使用通配符
            </tx:attributes>
        </tx:advice>
    	<aop:config>
            <aop:pointcut id="" expression=""/>
            <aop:advisor pointcut="" advice-ref="interceptor"/>
        </aop:config>
    ~~~



### web项目中的使用

- 把容器对象放到全局作用域ServletContext

- 监听器依赖

  ~~~xml
  <dependency>
              <groupId>org.springframework</groupId>
              <artifactId>spring-web</artifactId>
              <version>5.2.9.RELEASE</version>
          </dependency>
  ~~~

- web.xml注册ContextLoaderListener监听器





# SpringMVC

基于Spring的框架，用于web开发，底层是Servlet

### 加入依赖

~~~xml
<dependency>
            <groupId>javax.servlet</groupId>
            <artifactId>servlet-api</artifactId>
            <version>2.5</version>
        </dependency>
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-web</artifactId>
            <version>5.2.10.RELEASE</version>
        </dependency>
~~~



### 配置web.xml

~~~xml
<!-- spring配置 -->
    <!-- Spring加载的xml文件,不配置默认为applicationContext.xml -->
    <context-param>
        <param-name>contextConfigLocation</param-name>
        <param-value>/WEB-INF/springConfig.xml</param-value>
    </context-param>

    <!--spring mvc配置-->
    <!-- 配置Sping MVC的DispatcherServlet,也可以配置为继承了DispatcherServlet的自定义类,这里配置spring mvc的配置(扫描controller) -->
    <servlet>
        <servlet-name>springmvcservlet</servlet-name>
        <servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>
        <!-- spring MVC的配置文件 -->
        <init-param>
             <param-name>contextConfigLocation</param-name>
             <param-value>/WEB-INF/springmvc.xml</param-value>
        </init-param>
        <!--其他参数-->
        <init-param>
             <param-name>appName</param-name>
             <param-value>authplatform</param-value>
        </init-param>
        <!-- 下面值小一点比较合适，会优先加载 -->
        <load-on-startup>1</load-on-startup>
    </servlet>
    <servlet-mapping>
        <servlet-name>springmvcservlet</servlet-name>
        <url-pattern>/</url-pattern>
    </servlet-mapping>

    <!-- 配置请求过滤器，编码格式设为UTF-8，避免中文乱码 -->
    <filter>
        <filter-name>charsetfilter</filter-name>
        <filter-class>
            org.springframework.web.filter.CharacterEncodingFilter
        </filter-class>
        <init-param>
            <param-name>encoding</param-name>
            <param-value>UTF-8</param-value>
        </init-param>
        <init-param>
            <param-name>forceEncoding</param-name>
            <param-value>true</param-value>
        </init-param>
    </filter>
    <filter-mapping>
        <filter-name>charsetfilter</filter-name>
        <url-pattern>/*</url-pattern>
    </filter-mapping>

    <!-- 该类作为spring的listener使用，它会在创建时自动查找web.xml配置的applicationContext.xml文件 -->
    <listener>
        <listener-class>
            org.springframework.web.context.ContextLoaderListener
        </listener-class>
    </listener>

    <!-- 此监听器主要用于解决java.beans.Introspector导致的内存泄漏的问题 -->
    <listener>
        <listener-class>org.springframework.web.util.IntrospectorCleanupListener</listener-class>
    </listener>
~~~



### 配置Springmvc.xml

~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:mvc="http://www.springframework.org/schema/mvc"
       xmlns:context="http://www.springframework.org/schema/context"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
       http://www.springframework.org/schema/beans/spring-beans.xsd
        http://www.springframework.org/schema/mvc
       http://www.springframework.org/schema/mvc/spring-mvc.xsd
        http://www.springframework.org/schema/context
       http://www.springframework.org/schema/context/spring-context.xsd
    ">
    <context:component-scan base-package=""/>

    <bean class="org.springframework.web.servlet.view.InternalResourceViewResolver">
        <property name="prefix" value=""></property>
        <property name="suffix" value=""></property>
    </bean>

    <mvc:annotation-driven/>
    <mvc:resources mapping="resources/**" location="/resources/"/>
</beans>
~~~



### 注解

- @RequestMapping
- @Controller
- @ResponseBody（必须加入json处理依赖Jackson，开启注解驱动） 



### 解决静态资源问题

~~~xml
<mvc:annotation-driven/>
<mvc:default-servlet-handler/>


主要方式
<mvc:annotation-driven/>
<mvc:resources mapping="resources/**" location="/resources/"/>
<mvc:resources mapping="js/**" location="/js/"/>
....
~~~

- base标签





### SSM整合开发

- 将controller写在springMVC容器中，将dao、Service写在Spring容器中
- SpringMVC容器是Spring容器的子容器，类似继承



#### 步骤

一 创建Maven项目具体步骤如下：

二 配置文件

2.1 配置mybatis-config.xml

2.2 配置mapper.xml

2.3 配置jdbc.properties

2.4 配置applicationContext.xml

2.5 配置springmvc-servlet.xml

2.6 配置web.xml

2.7 配置log4j.properties

2.8 引入依赖

三 测试

3.1 创建java文件

3.1.1 UserController类

3.1.2 User实体类

3.1.3 UserService接口 

3.1.4 UserServiceImpl实现类

3.1.5 UserMapper类

3.2 创建MySql数据库表

3.3 创建users.jsp文



#### 依赖

~~~xml
<?xml version="1.0" encoding="UTF-8"?>

<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>

  <groupId>com.heyong</groupId>
  <artifactId>SSM</artifactId>
  <version>1.0-SNAPSHOT</version>
  <packaging>war</packaging>

  <name>SSM Maven Webapp</name>
  <!-- FIXME change it to the project's website -->
  <url>http://www.example.com</url>

  <properties>
    <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    <maven.compiler.source>1.8</maven.compiler.source>
    <maven.compiler.target>1.8</maven.compiler.target>
  </properties>

  <dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.11</version>
      <scope>test</scope>
    </dependency>


<!--    事务-->
    <dependency>
      <groupId>org.springframework</groupId>
      <artifactId>spring-jdbc</artifactId>
      <version>5.2.10.RELEASE</version>
    </dependency>

    <dependency>
      <groupId>org.springframework</groupId>
      <artifactId>spring-tx</artifactId>
      <version>5.2.10.RELEASE</version>
    </dependency>

    <dependency>
      <groupId>org.springframework</groupId>
      <artifactId>spring-webmvc</artifactId>
      <version>5.2.10.RELEASE</version>
    </dependency>

    <dependency>
      <groupId>org.springframework</groupId>
      <artifactId>spring</artifactId>
      <version>5.2.10.RELEASE</version>
      <type>pom</type>
    </dependency>




    <!-- json依赖-->
    <dependency>
      <groupId>com.cedarsoft.serialization</groupId>
      <artifactId>jackson</artifactId>
      <version>8.9.0</version>
    </dependency>
    <dependency>
      <groupId>com.fasterxml.jackson.core</groupId>
      <artifactId>jackson-core</artifactId>
      <version>2.11.3</version>
    </dependency>
    <dependency>
      <groupId>com.fasterxml.jackson.core</groupId>
      <artifactId>jackson-databind</artifactId>
      <version>2.11.3</version>
    </dependency>


<!--数据库依赖-->
    <dependency>
    <groupId>org.mybatis</groupId>
    <artifactId>mybatis-spring</artifactId>
    <version>2.0.5</version>
    </dependency>

    <dependency>
      <groupId>org.mybatis</groupId>
      <artifactId>mybatis</artifactId>
      <version>3.5.5</version>
    </dependency>

    <dependency>
      <groupId>mysql</groupId>
      <artifactId>mysql-connector-java</artifactId>
      <version>8.0.21</version>
    </dependency>

<!--    数据库连接池依赖-->
    <dependency>
      <groupId>com.alibaba</groupId>
      <artifactId>druid</artifactId>
      <version>1.1.10</version>
    </dependency>


<!--    servlet依赖-->
    <dependency>
      <groupId>javax.servlet</groupId>
      <artifactId>servlet-api</artifactId>
      <version>2.5</version>
    </dependency>
  </dependencies>

  <build>
    <resources>
      <resource>
        <directory>src/main/java</directory>
        <includes>
          <include>**/*.xml</include>
          <include>**/*.properties</include>
        </includes>
        <filtering>true</filtering>
      </resource>
      <resource>
        <directory>src/main/resources</directory>
        <includes>
          <include>**/*.xml</include>
        </includes>
        <filtering>true</filtering>
      </resource>
    </resources>
  </build>
</project>

~~~

#### web.xml

~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<web-app xmlns="http://xmlns.jcp.org/xml/ns/javaee"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://xmlns.jcp.org/xml/ns/javaee http://xmlns.jcp.org/xml/ns/javaee/web-app_4_0.xsd"
         version="4.0">

    <servlet>
        <servlet-name>myservlet</servlet-name>
        <servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>
        <init-param>
            <param-name>contextConfigLocation</param-name>
            <param-value>/WEB-INF/springMVC.xml</param-value>
        </init-param>
        <load-on-startup>1</load-on-startup>
    </servlet>

    <servlet-mapping>
        <servlet-name>myservlet</servlet-name>
        <url-pattern>/</url-pattern>
    </servlet-mapping>
	
    <context-param>
        <param-name>contextConfigLocation</param-name>
        <param-value>classpath:conf/applicationContext.xml</param-value>
    </context-param>
    <listener>
        <listener-class>org.springframework.web.context.ContextLoaderListener</listener-class>
    </listener>
    
    <filter>
        <filter-name>charsetfilter</filter-name>
        <filter-class>
            org.springframework.web.filter.CharacterEncodingFilter
        </filter-class>
        <init-param>
            <param-name>encoding</param-name>
            <param-value>UTF-8</param-value>
        </init-param>
        <init-param>
            <param-name>forceEncoding</param-name>
            <param-value>true</param-value>
        </init-param>
    </filter>
    <filter-mapping>
        <filter-name>charsetfilter</filter-name>
        <url-pattern>/</url-pattern>
    </filter-mapping>
</web-app>
~~~

#### springMVC配置文件

~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:context="http://www.springframework.org/schema/context"
       xmlns:mvc="http://www.springframework.org/schema/mvc"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
         http://www.springframework.org/schema/beans/spring-beans.xsd
        http://www.springframework.org/schema/context
        http://www.springframework.org/schema/context/spring-context-4.3.xsd
        http://www.springframework.org/schema/mvc
        http://www.springframework.org/schema/mvc/spring-mvc-4.3.xsd">

    <!-- 自动扫描包，实现支持注解的IOC -->
    <context:component-scan base-package="" />

    <!-- Spring MVC不处理静态资源 -->
    <mvc:default-servlet-handler />

    <!-- 支持mvc注解驱动 -->
    <mvc:annotation-driven />

    <!-- 视图解析器 -->
    <bean
            class="org.springframework.web.servlet.view.InternalResourceViewResolver"
            id="internalResourceViewResolver">
        <!-- 前缀 -->
        <property name="prefix" value="/WEB-INF/view/" />
        <!-- 后缀 -->
        <property name="suffix" value=".jsp" />
    </bean>
</beans>
~~~

#### spring配置文件

~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:context="http://www.springframework.org/schema/context"
       xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd http://www.springframework.org/schema/context https://www.springframework.org/schema/context/spring-context.xsd">

<!--    导入配置文件-->
    <context:property-placeholder location="conf/jdbc.properties"/>
<!--配置数据源-->
    <bean id="dataSource" class="com.alibaba.druid.pool.DruidDataSource">
        <property name="driverClassName" value="com.mysql.cj.jdbc.Driver"/>
        <property name="url" value=""/>
        <property name="username" value=""/>
        <property name="password" value=""/>
     </bean>

<!--    创建SqlSessionFactory-->
    <bean id="sqlSessionFactory" class="org.mybatis.spring.SqlSessionFactoryBean">
        <property name="dataSource" ref="dataSource"/>
        <property name="configLocation" value="classpath:conf/mybatis.xml"/>
    </bean>

<!--    声明mybatis扫描器-->
    <bean class="org.mybatis.spring.mapper.MapperScannerConfigurer">
        <property name="sqlSessionFactoryBeanName" value="sqlSessionFactory"/>
        <property name="basePackage" value=""/>
    </bean>

    <context:component-scan base-package=""/>

<!--    事务-->
</beans>
~~~



#### mybatis主配置文件

~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE configuration
        PUBLIC "-//mybatis.org//DTD Config 3.0//EN"
        "http://mybatis.org/dtd/mybatis-3-config.dtd">
<configuration>

<!--    &lt;!&ndash; 环境配置：事务管理器和数据源配置 &ndash;&gt;-->
<!--    <environments default="development">-->
<!--        <environment id="development">-->
<!--            <transactionManager type="JDBC" />-->
<!--            <dataSource type="POOLED">-->
<!--                <property name="driver" value="${jdbc.driver}" />-->
<!--                <property name="url" value="${jdbc.url}" />-->
<!--                <property name="username" value="${jdbc.username}" />-->
<!--                <property name="password" value="${jdbc.password}" />-->
<!--            </dataSource>-->
<!--        </environment>-->
<!--    </environments>-->

    <typeAliases>
        <package name=""/>
    </typeAliases>
    
    <!-- 映射器 -->
    <mappers>
        <package name="" />
    </mappers>
</configuration>
~~~



#### 数据库属性配置文件

~~~properties
jdbc.url=jdbc:mysql://localhost:3306/blog?severTimezone=Asia/Shanghai
jdbc.username=root
jdbc.password=heyong728350858
jdbc.Driver=com.
~~~

