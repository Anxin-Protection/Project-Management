# Project-Management
安芯守护项目管理
```mermaid
gantt
    title 项目日程表
    dateFormat YYYY-MM-DD
    section 准备工作
    人员框架图绘制 : done, OC, 2025-10-3, 1d12h
    成员信息收集 : MIC, after OC, 2d
    成员身份分配 : MA, after OC, 2d
    建立部长群和各部分群 : ES, after MA, 1d
    部长任务培训 : TT, after MA, 1d
    第一次线上会议 : FOM, after MA, 1d
    软件开发规范编写 : active, SDS, 2025-10-3, 2d
    硬件开发规范编写 : done, HDS, 2025-10-3, 1d
    部门职责要求编写 : done, DRR, 2025-10-3, 1d
    协同开发规范编写 : done, CDS, 2025-10-3, 1d
    section 试验性开发
    子机程序编写 : SHPD, 2025-10-11, 30d
    主机程序编写 : HPD, 2025-10-11, 30d
    服务器程序编写 : SPD, 2025-10-11, 30d
    功能验证 : FV, after SPD, 1d