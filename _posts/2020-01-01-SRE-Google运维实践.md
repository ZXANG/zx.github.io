---
title: 《SRE Google运维实践》介绍
description: 《SRE Google运维实践》 综述; Google SRE系列的第二本书。是对第一本书说描述的内容的更详细的解读。
categories:
 - SRE
tags: 《SRE-Google运维实践》 
---

> 《The Site Reliability Workbook — Practical Ways to Implement SRE》 


<!-- more -->

Edited by:
    Betsy Beyer, Niall Richard Murphy, David K. Rensin, Kent Kawahara and Stephen Thorne

## 前言


> The Site Reliability Workbook is the hands-on companion to the bestselling Site Reliability Engineering
> book and uses concrete examples to show how to put SRE principles and practices to work. This book contains 
> practical examples from Google’s experiences and case studies from Google’s Cloud Platform customers. 
> Evernote, The Home Depot, The New York Times, and other companies outline hard-won experiences of what 
> worked for them and what didn’t.


《The Site Reliability Workbook》操作手册 通过具体的案例来展示如何在工作中实践SRE。 本书包含了Google自身经历
或是从Google's Cloud Platform的客户案例。例如：Evernote、The Home Depot、The New York Times。


> ### <center>How to Read This Book</center>
> This book is the companion volume to Google’s first book, Site Reliability Engineering. To get the most out of this volume, we recommend that you have read, or can refer to, the first SRE book (available to read online for free at google.com/sre). The two works complement each other in the following ways:
> * The previous work was an introduction to principles and philosophy. This volume concentrates on how those principles are applied. (In a few areas—particu‐larly configuration management and canarying—we also cover some new ground to provide background for the practical treatment of other subjects.)
>
> * The earlier volume concentrated exclusively on how SRE is practiced at Google. This work includes perspectives from a number of other firms—from traditional enterprises (including The Home Depot and the New York Times) to digital natives (Evernote, Spotify, and others).
>
> * The first book didn’t directly refer to the larger operations community—especially DevOps—whereas this book speaks directly to how SRE and DevOps relate to each other.
> 
> This volume assumes that you will bounce between this volume and its predecessor.  You might, for example, read Chapter 4, “Service Level Objectives” in the first book and then read its implementation complement (Chapter 2) in this volume.
>
> This book assumes that every chapter is just the starting point for a longer discussion and journey. Accordingly, this book is intended to be a conversation starter rather than the last word.
> 
> —The Editors


> ### <center>如何阅读本书</center>
> 这本书是google第一本sre(Site Reliability Engineering)书的姊妹篇. 要充分读懂本书，我们建议您阅读或参考第一本SRE书籍(可在google.com/sre在线免费阅读)。这两部作品在以下几个方面是相辅相成的:    
> * 第一本书主要是是原则和理论的介绍。本书主要讨论如何应用这些原则。(在少数几个领域——主要是配置管理和灰度——我们还讨论了一些新领域，为其他主题的实际应用提供了场景。)
>
> * 第一本书专门集中于如何在谷歌实践SRE。包括许多其他公司的观点——从传统企业(包括家得宝和纽约时报)到`数字原生代`(Evernote、Spotify和其他)。
>
> * 第一本书没有直接提到更大的运营社区—特别是DevOps—而这本书直接谈到了SRE和DevOps是如何相互关联的。
> 
> 本书假设你会在阅读第一本书和第二本书之间互相验证。例如，您可以在第一本书中阅读第4章“服务级别目标”，然后在本卷中阅读(第2章)其实现补充。
>
> 本书假设每一章只是一个更长的讨论和旅程的起点。因此，本书的目的是要成为一个对话的开始，而不是结束。
> 
> —The Editors
 
> 备注：
>
>   数字原生代:是美国哈佛大学的网络社会研究中心和瑞士圣加仑大学的信息法研究中心提出的概念， 意为“80 后” 甚至再年轻些的这代人一出生就面临着一个无所不在的网络世界，对于他们而言，网络就是他们的生活，数字化生存是他们从小就开始的生存方式。


本书目录结构：

第一章  SRE与DevOps之间的联系
### 第一部分：基本原理  
第二章  SLO实施  
第三章  SLO工程案例学习  
第四章  监控  
第五章  SLO报警  
第六章  减少琐事  
第七章  简单化    
第八章  On-Call   
### 第二部分： 实践  
第九章   故障响应  
第十章   故障总结：从失败中学习  
第十一章  应对过载  
第十二章  非抽象大系统设计介绍  
第十三章  数据处理管道  
第十四章  系统配置最佳实践  
第十五章  配置细节    
第十六章  灰度发布（金丝雀部署）  
### 第三部分： 发展  
第十七章  从过载中识别和恢复     
第十八章  SRE：参与模式  
第十九章  SRE：超出界限  
第二十章  SRE：团队生命周期  
第二十一章  SRE：组织变更管理  

### SRE？
>
>  网站可靠性工程师（SRE）Site Reliability Engineering
>


### Google的SRE具体会负责哪些事情？
> 
> SRE在Google不负责某个服务的上线、部署，SRE主要是保障服务的可靠性和性能，同时负责数据中资源分配，为重要服务预留资源，SRE并不负责某个业务逻辑的具体编写，主要负责在服务出现宕机等紧急事故时，可以快速作出响应，尽快恢复服务，减少服务掉线而造成的损失。
>

### SRE日常工作和职责包含哪些?
>
> 一般来说，SRE团队要承担以下几类职责：可用性改进、延迟优化、性能优化、效率优化、变更管理、监控、紧急事物处理以及容量规划与管理。
> 
> Tools Don't create reliability. Humans do. But tools can help.
>


### 相关资料

英文原版：[the-site-reliability-workbook-next18.pdf](/blog/something/pdf/SRE/the-site-reliability-workbook-next18.pdf)  
悟冥：[读《SRE：Google运维解密》一点思考](https://zhuanlan.zhihu.com/p/97600369)  
SRE Google运维解密  

