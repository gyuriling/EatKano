<p align="center">
  <a href="https://xingye.me/game/eatkano"><img src="https://github.com/gyuriling/EatKano/blob/main/static/image/ClickBefore.png?raw=true" width="100" height="100" alt="EatKano"></a>
</p>
<div align="center">



# え？

</div>

[Play now](https://gyuriling.github.io/EatKano/) | 내 최고기록은 208 😗

누군가가 만든 완다호이에무 카노게임 보고 따라만든 카나데 게임 ! !  
이 프로젝트는 [arcxingye/EatKano](https://github.com/arcxingye/EatKano). 의 **customized fork** 버전입니다 🤤



## 可选功能

简易排行榜(日/周/月) 不推荐使用

不需要排行榜把php/sql文件都删掉即可

## 版本需求
+ MySQL 5+
+ PHP 5+

## 使用方法

注: 如果你想玩的话直接去玩就可以, 这里是如何制造你的改版

### 部署到服务器

按照这些步骤来在你的服务器上配置排行榜的数据库

1. 创建数据库并且执行提供的脚本(这里用`kano`作为数据库名)
   ```sql
   CREATE DATABASE kano DEFAULT CHARSET=utf8;
   USE kano;
   SOURCE kano.sql;
   ```

2. 更改有数据库信息的`conn.php`为你的数据库配置

   ```php
   <?php
   // 把这里改为你的配置
   $link = new mysqli('localhost','NAME','PASSWORD','kano');
   mysqli_set_charset($link, 'utf8');
   if ($link->connect_error) {
       die("Failed to connect: " . $conn->connect_error);
   }
   $ranking = "kano_rank";
   ```


## 其它事项

点下star吧~ 欢迎pr代码
