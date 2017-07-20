
[Spring思维导图，让Spring不再难懂（mvc篇）]
(https://my.oschina.net/u/3080373/blog/1438733)(梳理得很清晰)

[SpringMVC概述]
(http://www.cnblogs.com/wxisme/p/4926266.html)(有个处理流程图挺清晰的)

[Spring MVC 入门示例讲解]
(http://www.importnew.com/15141.html)(这个项目用tomcat7跑起来了)(git2这个项目是跑起来了的)(springmvcexample.zip)
[Spring4 MVC HelloWord实例]
(http://www.yiibai.com/spring_mvc/spring-mvc-tutorial-for-beginners.html)(改造了之后可以跑起来)(源文件springm.zip)


### web.xml
~~~XML
<web-app id="WebApp_ID" version="2.4"
	xmlns="http://java.sun.com/xml/ns/j2ee"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://java.sun.com/xml/ns/j2ee
	http://java.sun.com/xml/ns/j2ee/web-app_2_4.xsd">

	<display-name>Spring Web MVC Hello World Application</display-name>

	<servlet>
		<servlet-name>spring</servlet-name>
		<servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>
		<load-on-startup>1</load-on-startup>
	</servlet>

	<servlet-mapping>
		<servlet-name>spring</servlet-name>
		<url-pattern>/</url-pattern>
	</servlet-mapping>

</web-app>
~~~

### spring-servlet.xml
~~~XML
<beans xmlns="http://www.springframework.org/schema/beans"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xmlns:context="http://www.springframework.org/schema/context"
	xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans-3.0.xsd
        http://www.springframework.org/schema/context
        http://www.springframework.org/schema/context/spring-context-3.0.xsd">

	<context:component-scan base-package="com.yiibai" />

	<bean class="org.springframework.web.servlet.mvc.annotation.DefaultAnnotationHandlerMapping" />
	<bean class="org.springframework.web.servlet.mvc.annotation.AnnotationMethodHandlerAdapter" />

	<bean class="org.springframework.web.servlet.view.InternalResourceViewResolver">
	    <property name="prefix" value="/WEB-INF/pages/" />
	    <property name="suffix" value=".jsp" />
	</bean>


</beans>
~~~
