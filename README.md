# 安芯守护项目 GitHub 协同开发规范 -- 审核部版（附件在Adds下）

## 1.仓库架构

- **Project-Manager**：审查部专用仓库，存放时间表、计划表与备份
- **Devlop-Repository**：开发用仓库

``` markdown
Devlop-Repository/ （dev、main分支）
├── Adds/ # 本文件附件
├── Meeting/ # 会议记录
│   ├── Weekly # 每周例行全体会议（**周五开会，周日上学前上传**）
│   ├── Devlop # 开发人员会议（**对应的周日上学前上传**）
│   └── Others # 其他会议
├── Examination/ # 审核文件
│   └── YYYY-MM-DD # 按年月日新建文件夹，便于溯源
├── .git/
├── README.md # 协同开发规范文档
├── .gitignore
└── LICENSE

Devlop-Repository/ （history/YYYY-MM-DD 分支）# 按年月日命名，便于溯源
此分支下为 **开发用仓库 Project-Manager 的完整备份**，每月一次

```

## 2. 分支管理

- **主分支（main）**：仅存放审查部的稳定会议记录与已审核文件
- **开发分支（dev）**：日常以该分支作为下一次会议记录更新的起点
- **历史分支（history/YYYY-MM-DD）**：仅归档开发仓库dev分支的完整拷贝
- **临时分支（temp/XXXXXX）**：工作时使用的临时分支（XXXXXX 为 **工号** ）

## 3.日常工作流程

- 会议纪要上传（审核部同时负责会议的 **笔录工作** ）

1. 准备好已有的电子版材料、手写纸质版材料（需 **拍照** 留档，确保画面清晰、内容完整）
2. 打开 git 相关软件（Edge / Git Cmd / Github Desktop），确保本地仓库与远程仓库同步（e.g.执行 `git pull` 命令更新最新内容）
3. 以 **dev** 为基础新建 **临时分支**，命名格式建议为 `temp/meeting-notes-YYYY-MM-DD-会议主题`（e.g. `temp/meeting-notes-20251024-Weekly`）
4. 在 **临时分支** 上进行文件操作：将整理后的会议纪要（建议统一为 MarkDown 格式，命名规范同上）及相关附件（照片等）放入仓库指定目录（ **/Meeting/会议类型/日期** ，参见 仓库架构 ），并检查文件格式及命名是否易于理解
5. 提交修改：执行 `git add .` or 在网页上手动添加文件，`git commit -m "新增[会议主题]会议纪要（YYYYMMDD）"` 填写清晰提交信息 or 网页上手动上传，随后 `git push` 推送至远程临时分支
6. 提交 PR（**Pull Request**） 至 **dev** 分支，在 PR 描述中注明 **会议时间、参与人员、核心议题等关键信息** ，并微信通知部长层进行审核
7. 再审核通过后方可合并（ **merge** ）至 **dev** 分支，合并后删除临时分支（本地及远程），确保仓库分支整洁

- 审核项目开发方案、开发计划等（审核部同时负责审核会议的 **笔录工作** ）

``` text
Tips:策划部和开发部 所有 文件在上传至Github前 都 需要经过 审核部 组织相关人员进行审核
相关人员来源：部长层+部长层推荐人员
```

1. 发起审核需要 **提前一个礼拜** 申请，口头申请需要事后补记录
2. **审核部** 安排审核时间并通知相应人员，组建审核临时群（线上）/申请场地（线下），上传审核申请记录
3. 其余步骤按 `会议纪要上传` 处理

## 3. 提交规范

- 每次提交前请确保记录完整无缺漏
- 提交信息建议使用英文，格式如下：

``` plaintext
<type>(<scope>): <subject>
```

- type：meeting(会议记录)、examination(审核文件)
- scope：如 weekly、devlop、others、examination等
- subject：简要描述本次提交内容

- 示例：`meeting(weekly): add meeting record`

## 4. 其他约定

- 定期同步主分支记录，避免大规模冲突
- 具体文件格式在附件中有

---
