```
pom.xml
\---<project>
    +...<groupId|artifactId|properties|dependencies|...>
    +---<build>
    |   +---<plugins>
    |   |   +---plugin.A
    |   |   \---plugin.B
    |   |
    |   \---<pluginManagement>
    |       \---<plugins>
    |           +---plugin.B
    |           \---plugin.C
    |
    \---<reporting>
        \---<plugins>
            \---plugin.C
```

plugin.A
```
<plugin>
  <groupId></groupId>
  <artifactId></artifactId>
  <version></version>
  <executions>
    <execution>
      <id></id> 識別字
      <phase></phase> mvn's phase like clean install ...
      <goals> 執行哪些goal，會是artifact套件裡可執行的程序
          <goal></goal>
          <goal>...</goal>
      </goals>
      <inherited></inherited> 是否可被繼承(預設是true)
      <configuration>
        ... 會是artifact裡可設定的參數，要參考工具的DOC，要搭pluginManagement maven-project-info-reports-plugin 不然不會執行，我也不知為什
      </configuration> 一些參數的設定
    </execution>
    <execution>...</execution>
  </executions>
  <dependencies></dependencies>
  <inherited></inherited>
  <configuration></configuration>
</plugin>
```
