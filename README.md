# MC服务器项目总目录 & 指南文件
MC服务器构建、管理模板，旨在给出一个有详细改写基础说明，且能拆分服务端、客户端的体系。<br>
开发指南见下使用教程部分，结构、定义部分为文档收录结构分层使用。

本文档结构基于"Compass 0.1.0-alpha"撰写。

MC server construction and management template aims to provide a system with detailed rewrite basic instructions and the ability to split the server and client.<br>
The development guide can be found in the tutorial section below, and the structure section is the hierarchical use of the document collection structure.


the structure of this doc is following "Compass 0.1.0-alpha".<br><br>

## 结构 Structure
- **纯粹分类** **pure-classification**
  
  上级：我的世界<br>
  同级：任何我的世界服务器项目<br>
  下级：ImagEMappeR.org的我的世界服务器项目<br>

  Superior: MineCraft<br>
  Level: Any Minecraft server projects<br>
  Subordinate: ImagEMappeR.org's Minecraft Server projects<br><br>
  
- **模块属性** **modulization**
  
  前置：[Forge官方](https://files.minecraftforge.net/net/minecraftforge/forge/);[CurseForge官方](https://www.curseforge.com/);等。<br>
  同类：任意我的世界整合包、包组<br>
  附属：暂无<br>
  
  Prerequisite: [Forge Official](https://files.minecraftforge.net/net/minecraftforge/forge/);[CurseForge Official](https://www.curseforge.com/);<br>
  Homotype: Any MineCraft Integration Packages, or Package Groups<br>
  belongling: null(tentative)<br>

## 定义 Definition
ImagEMappeR.org的我的世界服务器项目总目录、指南文件<br>
Minecraft Server projects' directory and guide files, for ImagEMappeR.org

## 用途 Usage
ImagEMappeR.org的我的世界服务器项目总目录、指南文件，在使用教程部分规定本项目文件总的结构、开发模板，以便于不同开发人员基于统一规则的修改和自定义更新，以及为不同mod进行整合优化服务。<br>
ImagEMappeR.org原版权所有，以MIT.License为开源许可协议；您可以在[License文件夹](https://github.com/Liphael/MineCraft-Server-Projects/tree/main/License)中查看开源许可的所有内容。<br>

## 使用教程 Tutorial
如果没有过多精力、时间来详细研究教程内容，请参阅[快速开始](https://github.com/Liphael/MineCraft-Server-Projects/blob/main/README.md#%E5%BF%AB%E9%80%9F%E5%BC%80%E5%A7%8B-quickstart)部分。
### 立项 
#### 立项基本流程：
1. 在此目录下的[Projects](https://github.com/Liphael/MineCraft-Server-Projects/tree/main/Projects)文件夹目录下，建立一个**唯一的**仅属于该项目的子文件夹(下文简称**文件夹A**)，文件夹将包含项目所有历史内容；以“server_”开头，加上服务器项目的正式或暂定名称，来命名。<br>
2. 在**文件夹A**中，建立以[Semantic Versioning 2.0.0](https://semver.org/lang/zh-CN/)规则命名的发行(release)版本号子文件夹，对应每个发行版本的内容。<br>
3. 在**文件夹A**中，建立名为**README.md**的markdown文件，文件内容为下述**项目基本结构**部分中的**项目总规划**所述部分。<br>
4. 在**文件夹A**中，建立名为**PUSH_ADVICE.md**的markdown文件，文件内容为对**项目总规划**的修缮提议，内容格式无规则，自由记录想法。<br>
5. （预留，暂不实施）在**文件夹A**中，建立以该项目**哈希值编号**为名称的txt文件，用于识别和定位搜索项目。
6. 在发行(release)版本号子文件夹中，分别建立名为：**0-workbench**，**1-serverpack**，**2-clientpack**三个子文件夹；此三个文件夹从前到后的内容分别为：开发中源文件、服务器用整合包、客户端用整合包。
#### 其他注意事项：
* 开发人员对项目总规划的内容发生分歧时，若不能达成一致，应对分歧内容重新立项、命名。<br><br>

### 项目基本结构 Basic projects structure
#### 项目总规划
项目总规划的内容暂定为下述几个部分，为选取整合用mod、资源包以及自编源码等提供目的性指南：<br>
注：游戏中未作修改的部分空置不写即可；<br>
1. 总描述部分：以相对简洁的文字描述服务器整合包游戏体验的特征，玩法风格等。
2. 宏观重制部分：(暂定)包括**地图生成**、**制作系统**、**魔法系统**、**运行库**四个子部分。宏观重制中陈列的内容要求对游戏中原生的机制作出较大修改，否则可以简单列在体验优化部分中。
3. 体验优化部分：(暂定)包括**物品方块**、**实体机制**、**动画&插件**、**UI&交互**四个子部分。此处列出的优化为主要面向客户端资源包的、可选的优化，或者对游戏内容本身改动较小的部分。<br><br>

#### 包管理结构
本部分规定各发行版本文件夹中，1-serverpack和2-Clientpack目录下；管理整合包的统一结构。<br>
此规范旨在便于开发人员修改和优化整合包源码。<br>
1. 非压缩主文件夹：<br>
1.1 [overides文件夹](https://github.com/Liphael/MineCraft-Server-Projects/tree/main/Projects/server_temp/0.1.0-beta/1-serverpack/1.20.1_forge47.3.0/overrides)<br>
1.2 [manifest.json](https://github.com/Liphael/MineCraft-Server-Projects/blob/main/Projects/server_temp/0.1.0-beta/1-serverpack/1.20.1_forge47.3.0/manifest.json)<br>
   [manifest文件说明](https://github.com/Liphael/MineCraft-Server-Projects/blob/main/Projects/server_temp/0.1.0-beta/1-serverpack/1.20.1_forge47.3.0/README.md#manifestjson%E6%96%87%E4%BB%B6%E8%AF%B4%E6%98%8E)<br>
1.3 [modlist.html](https://github.com/Liphael/MineCraft-Server-Projects/blob/main/Projects/server_temp/0.1.0-beta/1-serverpack/1.20.1_forge47.3.0/modlist.html)<br>
   [modlist文件说明](https://github.com/Liphael/MineCraft-Server-Projects/blob/main/Projects/server_temp/0.1.0-beta/1-serverpack/1.20.1_forge47.3.0/README.md#modlisthtml%E6%96%87%E4%BB%B6%E8%AF%B4%E6%98%8E)<br>
   
3. 压缩件
4. [JAR档案](https://zh.wikipedia.org/wiki/JAR_(%E6%96%87%E4%BB%B6%E6%A0%BC%E5%BC%8F))
JAR档案拟定


## 快速开始 QuickStart


## 开源许可 License
[开源许可模板](https://github.com/Liphael/MineCraft-Server-Projects/blob/main/License/MIT-%E8%AE%B8%E5%8F%AF-%E7%AE%80%E4%B8%AD%E7%BF%BB%E8%AF%91.txt)<br>
本项目许可基于[MIT开源许可](https://opensource.org/license/mit/)撰写。<br>
The MIT License (MIT): https://opensource.org/license/mit/<br>
