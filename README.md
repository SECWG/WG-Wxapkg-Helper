<p align="center">
  <img width="128" height="128" alt="logo" src="https://github.com/user-attachments/assets/367f19ea-f95c-437c-8d1b-8440de11d74a" />
</p>

<h3 align="center">
  <b>WG-Wxapkg-Helper</b>
</h3>

<p align="center">
  一款Wxapkg文件检测分析辅助工具
</p>


## 1.简介

一款面向安全、开发的微信小程序包（wxapkg）分析工具，提供可视化的解包、工程还原、敏感信息检测等功能，帮助快速分析小程序源码结构和潜在风险点。

## 2.快速开始

前往 [Releases](../../releases) 页面下载对应平台的安装包。

1. 启动程序，输入授权码激活
2. 进入「程序配置」设置扫描目录，或点击「检测」自动识别微信小程序缓存路径
3. 进入「提取规则」，配置启用规则
4. 在工作区点击「刷新」扫描小程序列表
5. 选中小程序后依次执行：**解包 → 检测**

## 3.界面预览

<img width="1331" height="905" alt="image" src="https://github.com/user-attachments/assets/c3753891-f26f-4988-988e-5c2c139cca69" />

## 4.规则编写

规则文件存放在 `data/rules/` 目录，每个文件对应一种检测类型，扩展名为 `.rule`。

- 每行一条正则表达式
- `#` 开头为注释，空行忽略
- 支持完整 PCRE 语法（前瞻、后顾、命名捕获组等）
- 使用命名捕获组 `(?P<name>...)` 可只提取匹配的部分内容

<img width="1357" height="927" alt="image" src="https://github.com/user-attachments/assets/c84e3851-163f-4098-a20a-1134c2dbf64f" />

详细规则编写说明见 [`规则编写指南.md`](data/rules/规则编写指南.md)

## 5.免责声明

本工具仅供小程序研究、安全测试等合法用途。使用者须遵守相关法律法规，对使用过程中产生的任何直接或间接后果自行承担责任，本项目不承担任何法律与连带责任。
