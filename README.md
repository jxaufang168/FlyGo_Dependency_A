# FlyGo_Dependency_A
文档地址：https://www.flygo520.com/docs/maven/maven-1alv38qqer46v

# 创建Maven父项目

1、右键`New` -> 选择`Project...`

![创建父项目 步骤1](https://www.flygo520.com/uploads/maven/images/m_29b83fe3f04034389ddc6b78293e9d58_r.png#size=360x0)

2、选择 `Maven Project` -> 选择 `下一步`

![创建父项目 步骤2](https://www.flygo520.com/uploads/maven/images/m_f05cb2cf736c817a83b0a05f4f888bd2_r.png#size=360x0)

3、勾选`Create a simple project  (skip archetype selection)`-> 选择`下一步`

![创建父项目 步骤3](https://www.flygo520.com/uploads/maven/images/m_88023f621995d513fd20c9440faf3ab5_r.png#size=360x0)

4、填写相关信息，特别注意，父类项目有且只能选择 `Packaging` 为 `pom` 类型。

![创建父项目 步骤3](https://www.flygo520.com/uploads/maven/images/m_f37fcf1d15e0c99fca2dd6e01e8275d3_r.png#size=360x0)

# Maven父项目目录结构

![父类项目目录结构](https://www.flygo520.com/uploads/maven/images/m_312e8cc5335f1736fc707d82461e0faa_r.png#size=360x0)

# 创建Maven 子项目

1、右键`New` -> 选择`Project...`

![创建子项目 步骤1](https://www.flygo520.com/uploads/maven/images/m_29b83fe3f04034389ddc6b78293e9d58_r.png#size=360x0)

2、选择 `Maven Project` -> 选择 `下一步`

![创建子项目 步骤2](https://www.flygo520.com/uploads/maven/images/m_f05cb2cf736c817a83b0a05f4f888bd2_r.png#size=360x0)

3、勾选`Create a simple project  (skip archetype selection)`-> 选择`下一步`

![创建子项目 步骤3](https://www.flygo520.com/uploads/maven/images/m_88023f621995d513fd20c9440faf3ab5_r.png#size=360x0)

4、注意填写 `Parent Project` 的Maven项目信息

![创建子项目 步骤4](https://www.flygo520.com/uploads/maven/images/m_88a0b2c3ec681c2387be2e4a4224a1d6_r.png#size=360x0)

# 子项目的目录结构

子项目的目录结构和普通的目录结构相同
`pom.xml` 配置文件增加了 `<Parent>`标签

```bash
<parent>
	<groupId>com.flygo520</groupId>
	<artifactId>FlyGo_Parent_A</artifactId>
	<version>0.0.1-SNAPSHOT</version>
</parent>
```
![子项目的目录结构](https://www.flygo520.com/uploads/maven/images/m_2f0721636078106ea60c6a0f99160dde_r.png#size=360x0)

# 继承项目之间的关系

1. 父项目是pom类型.
2. 子项目jar或war,如果子项目还是其他项目的父项目,子项目也是pom类型.
3. 有继承关系后,子项目中出现 `<parent>` 标签
>[danger] 如果子项目和 `<groupId>` 和 `<version>` 与父项目项目,在子项目中可以不配置 `<groupId>` 和 `<version>`
4. 父项目pom.xml中是看不到有哪些子项目.在逻辑上具有父子项目关系.
>[success] 项目之间的继承，类似于java中的继承关系，父项目 `pom.xml` 添加的依赖关系，子项目继承父项目的依赖。

![父项目添加依赖包，子项目继承](https://www.flygo520.com/uploads/maven/images/m_12818d364e9dc1160e5d7d3916a7e57e_r.png#size=360x0)

# 演示Demo源码地址

https://github.com/jxaufang168/FlyGo_Dependency_A

