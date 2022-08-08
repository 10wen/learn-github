## issue 与 pr 模板的配置及应用 

> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [eryajf.github.io](https://eryajf.github.io/HowToStartOpenSource/pages/93f4c2/#pull-request)

> GitHub 开源项目维护协作指南

项目协作过程中，我们需要通过制定一些模板，从而简化协作者以及自己的维护工作，本文就介绍 issue 与 pr 的模板。

有一个仓库汇集了各种 issue 与 pr 模板，我们可以从中选取适合自己的：

*   项目：[github-issue-templates (opens new window)](https://github.com/stevemao/github-issue-templates)

[#](#issue) issue
-----------------

给项目配置 issue 模板，能够让普通使用者更加规范地提交 issue 内容，也便于我们更加高效地处理 issue。

接下来我来讲下如何配置项目的 issue 模板。

*   [官方文档 (opens new window)](https://docs.github.com/cn/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository)

官方提供的模板几乎做成了一个表单，其实有时候反而加重了提交者的心智负担，以下是我项目中使用的模板。

`template-bug：`

```
$ cat .github/ISSUE_TEMPLATE/issue-template-bug.md
---
name: 🐛 错误报告 | Bug Report
about: 请详细描述您使用过程中遇到的问题。| Please describe in detail the problems you encountered in the process of using.
title: "🐛 一些问题。。。 | [Bug] Some problem..."
labels: ["bug"]
---

<!-- 请在您提交 bug 之前，回答以下这些问题。 | Please answer these questions before you submit a bug. -->

#### 您使用的版本？ | Your usage version?

#### 您使用的场景？ | Your usage scenarios?

#### 您做了什么操作？ | What did you do?

#### 您遇到了什么问题？ | What are your problems?

#### 您期望的结果是怎样的？ | What is your expected outcome?
```

`template-feature：`

```
$ cat .github/ISSUE_TEMPLATE/issue-template-feature.md
---
name: 🚀 功能请求 | Feature Request
about: 请详细描述您期望的功能。 | Please describe in detail the features you expect.
title: "🚀 一些功能。。。 | [Feature]Some feature..."
labels: ["enhancement"]
---

<!-- 请在您提交期望的功能之前，回答以下这些问题。 | Please answer these questions before you submit the desired feature. -->

#### 您使用的场景？ | 1. Your usage scenarios?

#### 您期望的结果是怎样的？ | 2. What is your expected outcome?
```



`template-question:`

```
$ cat .github/ISSUE_TEMPLATE/question-report.md               
---
name: 🙋 问题交流 | Question Report
about: 在文档或讨论中没有回答的使用问题 | Usage question that isn't answered in docs or discussion
title: "🙋 问题交流。。。 | [Question] Some question..."
labels: ["question"]
---

## Question Report

- 搜索打开和关闭的 [GitHub 问题](https://github.com/eryajf/go-ldap-admin/issues)

请在提交问题之前回答这些问题，谢谢。 | Please answer these questions before submitting them. Thank you.

### 你使用了哪个版本？ | Which version did you use?

### 预期行为 | Expected behavior

### 实际行为 | Actual behavior

### 原因分析（如果可以） | Cause analysis (if possible)

### 问题重现步骤 | Steps to reproduce the problem
```



以及一个配置文件：

```
$ cat .github/ISSUE_TEMPLATE/config.yml        
blank_issues_enabled: false
contact_links:
  - name: 📜 官方文档 | GO Ldap Admin Doc
    url: http://ldapdoc.eryajf.net
    about: 关于项目的功能用法以及设计考量，都会在官网进行呈现，提交问题之前，请先阅读官方文档，如果还不能满足，则再提问题。
  - name: 👀 Github论坛 | GitHub Discussions
    url: https://github.com/eryajf/go-ldap-admin/discussions
    about: 如果您的问题不是功能或者错误，请转到讨论面板并在提交之前检索您的问题是否已经存在。
```



这样，文件只需要放置在 `.github/ISSUE_TEMPLATE` 目录下，GitHub 就会自动将之识别解析为模板了，新建 issue 的页面也变成如下模样：

![](https://cdn.staticaly.com/gh/eryajf/tu/main/img/image_20220726_205630.png)

[#](#pull-request) pull request
-------------------------------

这里分享一下我个人使用的 issue 提交模板：

```
$ cat .github/pull-request-template.md   
<!-- 请务必在创建PR前，在右侧 Labels 选项中加上label的其中一个: [feature]、[fix]、[documentation] 。以便于Actions自动生成Releases时自动对PR进行归类。-->

**在提出此拉取请求时，我确认了以下几点（请复选框）：**

- [ ] 我已阅读并理解[贡献者指南]()。
- [ ] 我已检查没有与此请求重复的拉取请求。
- [ ] 我已经考虑过，并确认这份呈件对其他人很有价值。
- [ ] 我接受此提交可能不会被使用，并根据维护人员的意愿关闭拉取请求。

**填写PR内容：**

-
-
-
```



这样每当有协作者提交 pr，都需要提前知晓一些预置信息，以及一些可能的情况。

还有一个很重要的点在于，鼓励协作者主动给自己的 pr 打标签分类，从而便于[自动构建 release](https://eryajf.github.io/HowToStartOpenSource/01.basic-content/pages/4abd22/) 的时候根据 label 归类 pr 信息。