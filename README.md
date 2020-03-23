# free-generator-code


基于FreeMarker、mybatis-generator的通用代码生成器，生成不仅限于java代码，还可生成任意你想要的语言代码。使用非常简单，你不需要编写java代码，内部包含许多ftl案例，你可以参考ftl案例来扩展自定义ftl模板。

**可以统一通过一个变量设置模板位置，也可以自定义对每个模板指定一个位置（通常适用于项目分包的情况）**


##!!!初始案例sql脚本!!!
+ **数据库初始脚本（数据库名为：nimei）.sql**（仅用于案例测试使用，并非必须导入）


##!!!参考案例!!!
+ 案例1：启动类为StartUpQuickstart.java
  + 配置所在目录：resources\fgcDbConfig\quickstartConfig
  + 模板所在目录：resources\fgcTemplate\quickstartExample
+ 案例2：启动类为StartUpQuickstart2.java
  + 配置所在目录：resources\fgcDbConfig\quickstart2Config
  + 模板所在目录：resources\fgcTemplate\quickstart2Example
+ 案例3：启动类为StartUpMybatisPlus.java（原mybatis-plus模板进行迁移适配）
  + 配置所在目录：resources\fgcDbConfig\third\mybatisPlusConfig
  + 模板所在目录：resources\fgcTemplate\third\mybatisPlusExample\tableTemplate
+ ....


+ 案例1效果图：
  + 图1  ![image](https://github.com/JonSnow592622272/my-image/blob/master/free-generator-code/anli1.jpg)

<hr>

# 版本更新内容：
+ master
  + 完善内容
+ 3.0.1
  + 增加达梦数据库生成代码案例（启动类为DaMengGenerator.java）
+ 3.0.0
  + 适配升级mybatis-generator最新版（1.4.0）
+ 2.0.1
  + 完善现有模板
+ 2.0.0
  + 移除“tuofengTableName”，使用className代替。如需使用可以在1.0.0的tag版本使用。
+ 1.0.0
  + 适配mybatis-plus模板（启动类为StartUpMybatisPlus.java，默认生成路径为“D:/fgc_test_ftl”，每个模板可以单独设置路径。未做包名相对路径，可参考“quickstart2”简单改造即可实现）
  + 增加许多模板
  

<hr>
  
#####清除空文件夹下的“.gitxxx”文件（用Git Bash Here打开执行）
find ./ -type f -name '.gitxxx' -delete

#####使能够上传空文件夹（用Git Bash Here打开执行）
find . \( -type d -empty \) -and \( -not -regex ./\.git.* \) -exec touch {}/.gitxxx \;
