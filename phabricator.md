# Phabricator使用

![Phabricator](./assets/tool.png)

## 审查代码（Audit & Review code）

* Author把写好的代码上传到GitHub，然后git自动同步到Phabricator;

* 审核者登录Phabricator, 看到Audit图标右侧有两个数字，左边在蓝色圆框的表示有问题的commit，
右边那个数字则表示待审核的commit;

![Audit](./assets/Audit.png)

* 点击Audit进去，左边灰色栏为筛选器，看见有Problem Commits和Required Audits 这两个标题。Problem Commits 标题下的commit表示有问题的Commit，未审查前就已经Raised Concern。Required Audits标题下表示待审核的commit;

* 点击Problem Commits下或Required Audits下的 commit，审核者就可以看到跟新前跟跟新后代码的变化。
Commit下分为三大部分：


    * 展示代码上交的详细信息：

	| Left        |  含义                    | right                 |  含义                    |
	|-------------| -------------------------|-----------------------|--------------------------|
	| Status 	  |	 代码的状态				 | Edit Commit           |  编辑提交项目            |
	| Auditors    |  代码的审核者            | Edit Maniphtest Tasks |  修改自己所属的任务      |  
	| Committed   |  代码上传的时间          | Download Raw Diff     |  下载源代码              |  
	| Author      |  代码作者                | Remove Red Flag       |  提醒自己的标签          |
	| Parents     |  简述代码的功能          | Aword Token           |  表情标签（可增加可撤销）| 
	| Branches	  |  代码所属那个项目的分支	 |					     |  						|
	| Tags        |  代码的标签              |                       |  						|
	| Projuects   |  代码所属的项目          |                 
	                  
![firstone](./assets/firstone.png)

![firsttwo](./assets/firsttwo.png)

   * 展示跟新前跟跟新后代码块的变化，右侧有个拉列表 View Options 其主要作用是，审查者根据自己的需求来展示代码。

![ViewOption](./assets/ViewOption.png)
   
   * 在最下边有个Creative Accounting, 审核者在审查代码完之后可在这发表自己的观点。

![comment](./assets/comment.png)


## 任务管理(Task Management)
1. 用户登录Phabrcator 点击Maniphest进去；
2. 


![Maniphest](./assets/Maniphest.png)

## Bug管理(Bug Tracking)
