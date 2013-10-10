# Phabricator使用

![Phabricator](./assets/tool.png)

## 审查代码（Audit & Review code）

* Author把写好的代码上传到GitHub，然后git自动同步到Phabricator;

* 审核者登录Phabricator, 看到Audit图标右侧有两个数字，左边在蓝色圆框的表示有问题的代码块，未审核前就引发了
审核者的担忧，右边那个数字则表示待审核的commit;

![Audit](./assets/Audit.png)

* 点击Audit进去，左边灰色栏为筛选器，看见有Problem Commits和Required Audits 这两个标题。

* 点击Problem Commits下或Required Audits下的 commit，审核者就可以看到更新前跟更新后代码的变化。

Commit下分为四个模块：

第一个模块为列出代码上交的详细信息：

* 列表如下：

	| Left        |  含义                    | right                 |  含义                    |
	|-------------|--------------------------|-----------------------|--------------------------|
	| Status 	  |  代码的状态				  | Edit Commit           |  编辑提交项目            |
	| Auditors    |  代码的审核者            | Edit Maniphtest Tasks |  管理自己所属的任务      |  
	| Committed   |  代码上传的时间          | Download Raw Diff     |  下载源代码              |  
	| Author      |  代码作者                | Remove Red Flag       |  提醒自己的标签          |
	| Parents     |  简述代码的功能          | Aword Token           |  表情标签（可增加可撤销）| 
	| Branches	  |  代码所属那个项目的分支  |					        |  						        |
	| Tags        |  代码的标签              |                       |  						        |
	| Projects    |  代码所属的项目          |                       |                          |
	                  
![firstone](./assets/firstone.png)

![firsttwo](./assets/firsttwo.png)
   
   * 点击Edit Commit,将会出现这个画面。

![Editcommit](./assets/Editcommit.png) 

   * 其主要作用是提交的代码块是所属哪个项目或修改其所属项目。

   * 点击Edit Maniphtest Tasks，将会出现这个画面。

![Editmaniphesttsks](./assets/Editmaniphesttsks.png)

   * 其主要作用是管理任务。
   * 其中Assighed to Me属性表示列出我的任务，Created By Me的属性为列出我创建的任务，All Open Tasks属性为列出我
   未完成的所有任务，All Tasks属性为列出所有的任务。

第二个模块包含两个部分，第一部分为User对代码块的评论，第二部分为列出代码块具体被修改的信息和他的历史信息。

![Two](./assets/two.png)

第三个模块为展示被修改文件里代码更新前跟更新后代码块的变化。

![Three](./assets/three.png)

   * 其中左边表示未更新前的原代码，右边为更新后的代码。
   颜色不同的地方就是修改前跟修改后的行，加深颜色为修改的部分。
  
   * 右侧有个拉列表 View Options。

![ViewOption](./assets/ViewOption.png)

   * Collapse File属性， 表示打开或关闭被修改的文件；Browse in Diffusion属性，表示在新的窗口打开源文件；
   View Standalone属性，表示异常处理，即不符合原本制定的规则。Show Row File属性，表示打开未改动前的源文件；
   Configure Editor属性，表示配置编辑器。

第四个模块可视为评论模块，
   在最下边有个Creative Accounting, 审核者在审查代码完之后可在这发表自己的观点。

![comment](./assets/comment.png)

   * Action 有Comment属性，表示评论；Add CCs属性，表示抄送；Add Auditors属性，表示增加审核者；Accept Commit属性，表示审核通过；
   Raise Concern属性，表示担忧代码改动后可能引起的不良后果。


## 任务管理(Task Management)

* 用户登录Phabrcator 点击Maniphest进去。
 
![Maniphest](./assets/Maniphest.png)

* 用户将看到一个灰色框和一个白色框，用户可以根据自己的需求而在灰色框选择或搜索。

![huise](./assets/huise.png)

* 白色框表示你当前的任务。

![renwu](./assets/renwu.png)

*选择其中一个任务进去。
*在右侧会出现

![renwuone](./assets/renwuone.png)

* Edit Task属性表示编辑任务，Merge Duplicates IN属性表示把一个或两个任务合并在一起。Create
Subtask属性表示新建一个子任务，子任务的情况可在Priority属性设置轻重缓急，Edit Dependencies的属性为继承关系，Edit Differential Revisions属性修正任务BUG的标签， Flag For Later属性为一个提醒标签，Award Token属性为表情评价。

*点击Edit Task将看到

![Edittask](./assets/Edittask.png)

*其中Title的属性为题目；Status的属性为任务的状态；Assigned To属性为给某个User分配任务；CC为项目的创建者；Priority的属性为任务级别的状态；
Visible To的属性为可见的，意思是说谁能看见的这个任务的；Editable By的属性为任务是来自哪个项目编辑的；Projects的属性为此任务来自哪个项目的；Description的属性为描述任务要求的。

* 最下边有一个Weigh in
 
![renwutwo](./assets/renwutwo.png)

* Ation属性里边描述的是任务的状态。

* 你可以在Comment里边发表自己的评论。 
## Bug管理(Bug Tracking)

* Bug管理其实就是一个任务，当代码中出现BUG时，管理者可把BUG上传到Audit,让所有的user来讨论，然后指点最适合的那个User去完成这个任务。

