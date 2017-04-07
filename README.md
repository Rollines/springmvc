本例子主要是通过学习别人的例子来创建的：
使用技术：
Spring 4.0.6.RELEASE
validation-api 1.1.0.Final
hibernate-validator 5.1.2.Final
Bootstrap v3.1.0
Maven 3
JDK 1.6
Tomcat 7.0.54
Eclipse JUNO Service Release 2
涉及到的知识点主要有：
1、用Spring表单标签， 表单验证使用 JSR303 的验证注解，hibernate-validators，提供了使用MessageSource和访问静态资源(如CSS，JavaScript，图片)国际化支持我们的视图，使用ResourceHandlerRegistry，全部采用基于注解的配置。
2、首先要注意这里是 maven-war-plugin 插件声明。由于我们使用的是全注解配置，
我们甚至不包括在 web.xml 中，所以我们需要配置这个插件，以避免Maven构建war包失败。在验证部分 validation-api 代表规范， 而hibernate-validator是本规范的一个实现。hibernate-validator还提供了一些它自己的注解(@Email，@NotEmpty等)不属于规范的一部分。
