Chapter 04. 安装 Gradle
===================

## 4.1 前置条件

Gradle 需要 Java JDK 或者 JRE，版本为 6 及以上（可以使用`java -version`命令检查）。Gradle 附带了自己的 Groovy 库，因此 Groovy 不需要安装。任何已存在的 Groovy 安装将会被忽略。

Gradle 首先使用当前路径下的 JDK。或者，你可以设置一个`JAVA_HOME`环境变量指向你安装的 JDK 目录。

## 4.2 下载

可以从[Gradle web site][1]下载 Gradle 的发布包。

## 4.3 解压

Gradle 发布包通常是一个 ZIP 文件。它包含如下内容：

* Gradle 二进制文件。
* 用户向导（HTML 和 PDF 格式）。
* DSL 参考手册。
* API 文档（Javadoc 和 Groovydoc）。
* 基本实例，包括用户指南中的实例参考，也包含一些完整的更复杂的构建，你可以将其作为一个构建起点。
* 二进制源文件，这只是为了参考。如果你想编译 Gradle ，你可以下载源文件发行包或者从代码仓库中检出源文件。可以从[Gradle web site][1]获取更多细节。

## 4.4 环境变量

运行 Gradle，可以将`GRADLE_HOME/bin`添加到你的`PATH`环境变量中，通常这样就够了。

## 4.5 运行及测试安装

使用`gradle`命令运行 Gradle。检查 Gradle 是否被正确安装只需输入`gradle -v`命令。然后将会输出 Gradle 版本以及本地环境配置（包括 Groovy，JVM 版本，操作系统等等）。显示的版本应当与你下载的版本一致。

## 4.6 JVM 选项

运行 Gradle 的 JVM 选项可以通过设置环境变量实现。你可以使用 `GRADLE_OPTS` 或者 `JAVA_OPTS`，或者两者都用。`JAVA_OPTS` 和 Java 应用共享环境变量。典型的案例是在`JAVA_OPTS`设置 HTTP 代理，在 `GRADLE_OPTS` 设置内存。这些变量也可在 `gradle` 或者 `gradlew` 脚本开始时设置。

注意，目前无法在命令行工具中为 Gradle 设置 JVM 选项。

[1]: http://www.gradle.org/downloads
