## PR与issue的联动维护

> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [eryajf.github.io](https://eryajf.github.io/HowToStartOpenSource/pages/fa134e/)

> GitHub 开源项目维护协作指南

当我们需要解决项目中的一个 bug 时，通常一个新的`PR`会伴随一个`issue`，本文将介绍仅需通过创建`PR`时一个操作，关联上`issue`，然后当`PR`被同意之后，对应关联的`issue`也将随之关闭。

同样，我先在示例项目中创建一个`issue`：

![](https://cdn.staticaly.com/gh/eryajf/tu/main/img/image_20220719_145415.png)

这种时候，作为项目维护者，我们可以直接点击`Development`中的 `Create a branch` 创建一个 fix 分支，这样会自动关联上这个`issue`，同理，当该 fix 分支创建的`PR`被合并之后，`issue`也会自动关闭。

不过这里不讲此种方案，大家有兴趣可以自行体验一番。

这里讲的是我们更常见的一种操作，在本地编辑器里，基于最新的`main分支`切出一个`fix`分支，如下：

```
git checkout main
git pull
git checkout -b fix_testbug
```



然后就是在`fix_testbug`分支上进行对应问题的修复，这块儿不对赘述。

当我们感觉修复没问题了，也进行过自测了，就可以将此临时分支进行提交：

```
git add .
git commit -m "fix: test bug"
git push --set-upstream origin fix_testbug
```



推到远程之后，我们来到 GitHub 页面中，此时可以看到 GitHub 会自动提示一个新的分支可以合并：

![](https://cdn.staticaly.com/gh/eryajf/tu/main/img/image_20220719_150429.png)

可以直接点击`Compare & pull request`：

![](https://cdn.staticaly.com/gh/eryajf/tu/main/img/image_20220719_151051.png)

注意右侧`Development`中的说明，我们可以通过在说明中添加一些[关键字 (opens new window)](https://docs.github.com/cn/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue)，从而对`issue`进行关联，并触发关闭。当然也可以先创建 PR，然后再进行关联也可以：

![](https://cdn.staticaly.com/gh/eryajf/tu/main/img/image_20220719_151313.png)

完成关联的 PR，可以看到有这样的状态显示：

![](https://cdn.staticaly.com/gh/eryajf/tu/main/img/image_20220719_151423.png)

这个时候，我们点击到`#21`号`issue`中，也可以看到被关联到该`PR`上了：

![](https://cdn.staticaly.com/gh/eryajf/tu/main/img/image_20220719_151547.png)

现在我们将 `#23` 号`PR`进行合并，合并之后可以看到关联的`issue`也被关闭了，此次关联的临时分支也被删除了：

![](https://cdn.staticaly.com/gh/eryajf/tu/main/img/image_20220719_151825.png)

以上就是项目协同中，`PR`与`issue`的联动维护。

**另外：** 这里插一个小点，当我们完成一次 PR 流程之后，作为项目主维护人，通常会再次切回到 main 分支，然后将远程被合并到 main 分支的代码拉到本地：

```
git checkout main
git pull
```



这样执行之后，会发现本地代码竟然已经超过远程分支了：

![](https://cdn.staticaly.com/gh/eryajf/tu/main/img/image_20220719_154112.png)

其中的 389fe 那次是当前远程分支的 ID，我们可以执行如下命令，与远程对齐：

```
$ git reset --hard origin/main    
HEAD is now at 389fe7b fix: test bug (#23)
```



这样本地与远程就实现了对齐，在下次重新切分支，然后提交 PR 的时候，就不会出现上边那种，带了`几次Merge`的情况了。

图示如下：

![](https://cdn.staticaly.com/gh/eryajf/tu/main/img/image_20220719_154244.png)

理论上这次只有一个提交，而不应该出现 3 个`commit`，就是这个原因。