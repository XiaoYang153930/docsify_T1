# **Spring 基于构造函数的依赖注入（二）**

**constructor-arg子标签：**

**ref子标签：对应ref属性，该标签name属性的属性值为另一个bean标签id或name属性的属性值；**

**value子标签：对应value属性,用于设置基本数据类型或String类型的参数值；**

**list子标签：为数组或List类型的参数赋值**

**set子标签：为Set集合类型参数赋值**

**map子标签：为Map集合类型参数赋值**

**props子标签：为Properties类型的参数赋值**

## 数组类型

<bean class="live.sunhao.vo.Student"> <constructor-arg> <array> <value>18</value> <value>Rechel</value> <ref bean="d"/> <bean class="java.lang.String"> <constructor-arg value="String"></constructor-arg> </bean> </array> </constructor-arg> </bean>

## List集合

<bean class="live.sunhao.vo.Student"> <constructor-arg> <list> <value>12</value> <value>Tomcat</value> <ref bean="d"/> <bean class="java.lang.String"> <constructor-arg value="This is a list"></constructor-arg> </bean> </list> </constructor-arg> </bean>

## Set集合

<bean class="live.sunhao.vo.Student"> <constructor-arg> <set> <value>12</value> <value>Tomcat</value> <ref bean="d"/> <bean class="java.lang.String"> <constructor-arg value="This is a set"></constructor-arg> </bean> </set> </constructor-arg> </bean>

## Map集合

<bean class="live.sunhao.vo.Student"> <constructor-arg> <map> <entry key="name" value="myself"></entry> <entry key="age" value="22"></entry> <entry key="now" value-ref="da"></entry> </map> </constructor-arg> </bean>

## Properties

<bean class="live.sunhao.vo.Student"> <constructor-arg> <props> <prop key="driver">com.mysql.jdbc.Driver</prop> <prop key="userName">root</prop> <prop key="password">root</prop> <prop key="url">jdbc:mysql://127.0.0.1:3306/test</prop> </props> </constructor-arg> </bean>