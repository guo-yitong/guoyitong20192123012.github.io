## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/guo-yitong/guoyitong20192123012.github.io/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/guo-yitong/guoyitong20192123012.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.


图书系统管理用例图说明
1.	参与者
A.系统管理员   B.图书馆工作人员   C.教职员工   D.学生
2.	元素
四类参与者（详见第1条）
十七个用例（详见第3条）
十五条参与者与用例的关联关系
四条用例间的泛化关系
六条用例间的依赖关系（详见第3条）
3.	关系
参与者间的泛化关系：无

参与者与用例的关联关系：

                                      注册新员工人员账号

                                      用户锁定与解锁

                                      密码修改

    系统管理员                        密码找回

                                      新增读者信息

                                      修改用户信息

                                      用户信息查询

                                      登陆

                                      新增读者信息
    图书馆工作人员
                                      用户信息查询

                                      用户修改自己的密码

                                      登陆
    教职员工
                                      用户修改自己的密码

                                      登陆
    学生
                                      用户修改自己的密码

用例间的泛化关系：

                                      管理员重置用户密码
密码修改
                                  用户修改自己的密码

                                  修改各类用户信息
修改用户信息
                                  修改基本读者信息

用例间的依赖关系：

                      《extend》      密码找回
    登录
                      《extend》      自动锁定

               《include》        新增学生信息
新增读者信息
               《include》        新增教职工信息

                          《extend》       借书记录
用户信息查询
                          《extend》       违规记录

4.	建模思路
①	 该模块的主要使用者为：系统管理员、图书馆工作人员；
② 所有合法的用户账号都能正确登录到本系统中，如：登录时提供密码找回功能，可通过注册时
提供的邮箱地址，将重置后的密码发送到注册邮箱中。在登录时如果同一账号连续三次密码输入
错误则自动锁定该账号；

③ 用户密码修改功能，用户能自己修改密码，也可以通过管理员来实现用户密码重置；

④ 注册新工作人员账户，由管理员负责添加，这类用户需要提供的信息包括：账号名、密码、姓
名、性别、邮箱、电话号码；

⑤ 新增读者信息，管理员与图书馆工作人员都可以新增这类用户，这类用户又分为教职员工与学
生，其中教职员工需要提供的信息包括：借书证号、账号名、密码、姓名、性别、年龄、所在部
门、邮箱、电话号码、职务、专业；学生类账户需要提供的主要信息包括：借书证号、账号名、
密码、姓名、性别、所在系部、邮箱、电话号码、职务、专业、班级、身份证号、学号、开户日
期、状态等；

⑥ 修改用户信息，管理员能对各类用户信息进行修改，图书馆工作人员可以对读者的基本信息进
行修改；

⑦ 用户锁定与解锁功能，用户一旦被锁定就不能登录到本系统中，直到解锁为止；

⑧ 用户信息查询功能，能根据姓名、借书证号、所在部门查询用户的信息，并且在需要时还可以
查询指定用户的借书记录与违规记录等信息。

