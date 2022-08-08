## 个人GitHub主页配置

> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [eryajf.github.io](https://eryajf.github.io/HowToStartOpenSource/pages/f4ffde/#%E5%B1%95%E7%A4%BA)

> GitHub 开源项目维护协作指南

我很早注意到，GitHub 当中，你创建一个与自己账号同名的仓库，然后这个仓库的内容会展示在个人主页，换言之，你可以通过装扮这个仓库，来实现个人主页的装扮。

曾经也做过一些装扮的事情，只是很多内容还停留在表面，以至于主页看起来比较简单，最近对主页进行了整体的改造，过程中也遇到不少好的经验，这篇文章就是对这些内容的总结整理，看完之后，你也可以快速构建一个美观简洁的个人主页，这是一张重要的个人名片，快装扮起来吧。

我的个人主页：[https://github.com/eryajf (opens new window)](https://github.com/eryajf)

> 题外话：在折腾主页的过程中，我发现一个现象，国内的程序员折腾个人主页的比例要远远小于国外，也许，正是因为国内程序员都被困在 996 当中而失去了生活的情趣罢，再一次，旗帜鲜明地反对 996。

[#](#展示) 展示
-----------

![](https://cdn.staticaly.com/gh/eryajf/tu/main/img/image_20220722_102304.png)

[#](#参考) 参考
-----------

我们制作个人主页的第一步，在没有思路的时候，首先可以做的，就是参考别人的做法，先从模仿开始，然后再从模仿的过程中，逐渐摸索出能够展示自己个性的一套主页。

*   首先你可以参考我的主页全部配置，来进行个人主页的折腾配置。
*   GitHub 中也有不少搜集了优秀配置的仓库，这里列举一二：
    *   [awesome-github-profile-readme-chinese (opens new window)](https://github.com/eryajf/awesome-github-profile-readme-chinese)：由我整理的优秀的中文区个人主页搜集, 特别推荐。
    *   [awesome-github-profile-readme (opens new window)](https://github.com/abhisheknaiidu/awesome-github-profile-readme)：收集了大量的优秀案例，可供参考。
    *   [awesome-github-profile-readme-templates (opens new window)](https://github.com/durgeshsamariya/awesome-github-profile-readme-templates)：整理了大量的优秀模板，可供参考。
    *   [creative-profile-readme (opens new window)](https://github.com/coderjojo/creative-profile-readme)：又一个整理了大量案例的仓库。

还有一些能够在线制作个人 profile 的项目网站，非常优秀，这里列举如下：

*   项目：[profile-readme-generator (opens new window)](https://github.com/maurodesouza/profile-readme-generator) | 在线：[https://profile-readme-generator.com/ (opens new window)](https://profile-readme-generator.com/)
*   项目：[github-profile-readme-maker (opens new window)](https://github.com/VishwaGauravIn/github-profile-readme-maker) | 在线：[https://gprm.itsvg.in/ (opens new window)](https://gprm.itsvg.in/)

[#](#折腾) 折腾
-----------

接下来我讲下个人主页的内容是如何制作的，以给想要参考的同学一个思路。

### [#](#开头的动图) 开头的动图

效果如下：

![](https://camo.githubusercontent.com/b6e14b7547c87bf0cbdbf8e1f7db369f8b2bbade7ebf7d70be00dd054cf361ed/68747470733a2f2f726561646d652d747970696e672d7376672e6865726f6b756170702e636f6d3f666f6e743d48616e646c65652663656e7465723d74727565267643656e7465723d747275652677696474683d353030266865696768743d3630266c696e65733d5468652b74726176656c65722b6f6674656e2b617272697665732532432b616e642b7468652b646f65722b6f6674656e2b73756363656564732e)

此功能基于如下项目构建：

*   源码：[readme-typing-svg (opens new window)](https://github.com/DenverCoder1/readme-typing-svg)
*   在线：[readme-typing-svg-demo (opens new window)](https://readme-typing-svg.herokuapp.com/demo/)

你可以在在线工具中制作个人想要展示的内容。

### [#](#内容与构图) 内容与构图

前边内容就不多说了，每个人根据自己的实际想法撰写即可，图片也是基于 HTML 的右置语法实现。如下：

![](https://github.com/eryajf/tu/blob/main/img/image_20220626_200153.gif?raw=true)

### [#](#欢迎来访部分) 欢迎来访部分

此处内容分两部分，一个是访问次数计数，一个是其他图标内容的展示。

访问次数功能基于如下项目构建：

*   源码：[visitor-badge (opens new window)](https://github.com/hehuapei/visitor-badge)
*   在线：[visitor-badge-online (opens new window)](https://visitor-badge.laobi.icu/)

后边的图标内容根据如下网站提供能力构建：

*   [shields (opens new window)](https://shields.io/)

### [#](#语言工具) 语言工具

语言工具部分配置也比较简单，不过想要搜集齐自己的语言工具包，也是需要耗费一番功夫的。

其中图标功能基于如下项目配置：

*   源码：[devicon (opens new window)](https://github.com/devicons/devicon)
*   在线：[devicon.dev (opens new window)](https://devicon.dev/)

如果有图标在里边搜索不到，可以自己去对应语言或者工具的官网寻找 icon 图标。

我们还可以直接通过在线工具配置生成：

*   源码：[github-profile-readme-generator (opens new window)](https://github.com/rahuldkjain/github-profile-readme-generator)
*   在线：[readme-generator-online (opens new window)](https://rahuldkjain.github.io/gh-profile-readme-generator/)

### [#](#状态汇总统计) 状态汇总统计

状态汇总建议你不必过多纠结，直接参照我的配置，将 owner 名字替换就 OK 了：

```
![二丫讲梵's github stats](https://github-readme-stats.vercel.app/api?username=eryajf&hide_title=false&hide_border=true&show_icons=true&include_all_commits=true&line_height=20&bg_color=0,EC6C6C,FFD479,FFFC79,73FA79&theme=graywhite&locale=cn)![主要使用语言](https://github-readme-stats.vercel.app/api/top-langs/?username=eryajf&hide_title=false&hide_border=true&layout=compact&bg_color=0,73FA79,73FDFF,D783FF&theme=graywhite&locale=cn)

![profile](https://github-profile-trophy.vercel.app/?username=eryajf&theme=algolia&column=8)
```



其中状态汇总基于如下项目构建：

*   源码：[github-readme-stats (opens new window)](https://github.com/anuraghazra/github-readme-stats)
*   中文：[README (opens new window)](https://github.com/anuraghazra/github-readme-stats/blob/master/docs/readme_cn.md)

奖杯功能基于如下项目构建：

*   源码：[github-profile-trophy (opens new window)](https://github.com/ryo-ma/github-profile-trophy)
*   可根据说明文档自行调整配置。

### [#](#动态贪吃蛇) 动态贪吃蛇

首先看配置内容：

```
![snake](./assets/github-contribution-grid-snake.svg)
```

1  

引用了仓库本地的一个 svg 文件，此文件借助一个`GitHub Actinos`每天自动生成一次。

配置如下：

```
name: Generate Snake
on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2.3.4
      - name: Generate Snake
        uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: ${{ github.repository_owner }}
          gif_out_path: ./assets/github-contribution-grid-snake.gif
          svg_out_path: ./assets/github-contribution-grid-snake.svg
      - name: Push to GitHub
        uses: EndBug/add-and-commit@v7.2.1
        with:
          branch: master
          message: "Generate Contribution Snake"
```



此功能基于如下项目构建：

*   源码：[snk (opens new window)](https://github.com/Platane/snk)
*   在线：[snk-online (opens new window)](https://platane.github.io/snk/)

### [#](#提交动态折线图) 提交动态折线图

配置内容如下：

```
![](https://activity-graph.herokuapp.com/graph?username=eryajf&theme=github)
```

1  

如果你觉得我用的样式可以，那么直接替换 username 就可以生成你自己的。

此功能基于如下项目构建：

*   源码：[github-readme-activity-graph (opens new window)](https://github.com/Ashutosh00710/github-readme-activity-graph)
*   在线：[github-readme-activity-graph-online (opens new window)](https://ashutosh00710.github.io/github-readme-activity-graph/)

### [#](#类似github-pinned的功能) 类似 GitHub Pinned 的功能

GitHub Pinned 是一个能够将项目钉在个人主页的功能，效果如下：

![](https://cdn.staticaly.com/gh/eryajf/tu/main/img/image_20220722_111857.png)

但有一个问题，此功能只允许我们添加 6 个项目钉在这里。

通过如下配置，我们可以将更多自己想要钉住的项目钉在个人主页：

```
[![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=eryajf&repo=ldapctl&show_owner=true&&theme=cobalt)](https://github.com/eryajf/ldapctl)
```

1  

此功能基于如下项目构建：

*   源码：[github-readme-stats (opens new window)](https://github.com/anuraghazra/github-readme-stats)
*   中文：[README (opens new window)](https://github.com/anuraghazra/github-readme-stats/blob/master/docs/readme_cn.md#github-%E6%9B%B4%E5%A4%9A%E7%BD%AE%E9%A1%B6)

### [#](#博客最近更新) 博客最近更新

此处功能是基于 GitHub Actions 实现，每个小时运行一次，通过订阅博客的 RSS 将博客最近更新的几篇文章列举在此：

GitHub Actions 配置如下：

```
name: Latest blog post workflow
on:
  schedule: # Run workflow automatically
    - cron: '0 * * * *'
  workflow_dispatch:
jobs:
  update-readme-with-blog:
    name: Update this repo's README with latest blog posts
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Pull in eryajf posts
        uses: gautamkrishnar/blog-post-workflow@v1
        with:
          max_post_count: 6
          committer_username: "eryajf"
          committer_email: "eryajf@163.com"
          feed_list: "https://wiki.eryajf.net/rss.xml"
          template: "$newline- $randomEmoji(💯,🔥,💫,🚀,🌮,📝,🥳,💻,🧰,🏊,🥰,🧐,🤓,😎,🥸,🤩,🤗,🤔,🫣,🤭,🤠,👹,👺,🤡,🤖,🎃,😺,🫶,👍,💪,💄,👀,🧠,🧑‍🏫,👨‍🏫,💂,🧑‍💻,🥷,💃,🕴,💼,🎓,🐻,🐵,🙉,🦄,🦆,🦅,🦍,🦣,🐘,🦒,🦏,🐎,🦩,🐲,🌝,🌜,🌏,🌈,🌊,🎬,🎭,🚀,🚦,⛽️,🗽,🎡,🌋,🌁,💡,🕯,🪜,🧰,⚗️,🔭,🪄,🎊,🎉,) [$title]($url) $newline"
```



此功能基于如下项目构建：

*   源码：[blog-post-workflow (opens new window)](https://github.com/gautamkrishnar/blog-post-workflow)

以上就是我个人主页配置的全部内容了。

最后有以下几点内容想表达：

*   几乎每个功能都依赖于开源项目的实现，开源的魅力，正在于，我用你的开源，你用我的开源！
    
*   我想，个人主页的一大乐趣，正在于折腾，折腾之乐，无穷尽也！
    
*   也但愿国内开发者的个人主页早日遍地开花，百家争鸣起来！！