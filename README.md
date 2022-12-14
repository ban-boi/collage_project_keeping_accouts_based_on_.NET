![](media/f97678cc5ad9aa3fe86bc3f7b69531d2.jpeg)

课程设计

![](media/6673add3aab2a08803db3819b964a57c.jpeg)

| **学  院**   | 电气电气工程学院                     | **专  业**   | 计算机科学与技术 |
|--------------|--------------------------------------|--------------|------------------|
| **姓  名**   | ban_boi                               | **班  级**   | 0211191          |
| **设计名称** | 计算机软件综合项目——校内组队记账系统 |              |                  |
| **设计周数** | 2周                                  | **指导老师** | 老师好           |
| **起止时间** | 2022年6月22日\~2022年7月1日          |              |                  |

**  
目 录**

[一 校内组队记账软件需求和可行性分析](#_Toc107594319)

[**（一）需求分析**](#一需求分析)

[**（二）可行性分析**](#二可行性分析)

[二 校内组队记账软件总体设计](#二-校内组队记账软件总体设计)

[**（一）架构设计**](#一架构设计)

[**（三）角色设计**](#三角色设计)

[**（四）开发和运行平台选择**](#四开发和运行平台选择)

[**（五）数据库设计**](#五数据库设计)

[三 校内组队记账软件实现](#三-校内组队记账软件实现)

[**（一）用户管理模块**](#_Toc107594328)

[**（二）队伍管理管理模块**](#二队伍管理管理模块)

[**（三）队内操作模块**](#三队内操作模块)

[**（三）在线帮助模块**](#三在线帮助模块)

[四 校内组队记账软件测试](#四-校内组队记账软件测试)

[**（一）用户管理**](#一用户管理)

[**（二）队伍管理**](#二队伍管理)

[**（三）队内管理**](#三队内管理)

[**（四）在线帮助**](#四在线帮助)

[五 校内组队记账软件开发总结](#五-校内组队记账软件开发总结)

[**（一）主要功能**](#一主要功能)

[**（二）主要用途**](#二主要用途)

[**（三）技术特点**](#三技术特点)

[**（四）下一步工作**](#四下一步工作)

一 校内组队记账软件需求和可行性分析

## **（一）需求分析**

众所周知，国内疫情管控逐渐常态化。以上海为例，所有高校的食堂已经停止了堂食的服务长达三月之久，校内超市也只在规定时间内有序开放。为节约时间，也为减少人流聚集，“一人打多份饭”的模式在学校内较为流行。在这样的背景下，记账系统有着巨大的潜在需求市场和广大的应用空间。比如，一个寝室内的同学可以组成一组，轮流去买饭或物资并记在账上；同个实验室的不同年级的学生，也可以组成一组，实施相同的模式。使用记账系统既使得碍于情面不便催账的情况不复存在，也能免去繁杂的人工计算与多次的转账，若加以宣传，必然会受到校内广大学生的青睐，为学生的生活提供不少便捷。

## **（二）可行性分析**

技术可行性：

开发项目的功能、性能已在前文需求分析中列出。开发条件为如下，已有的硬件资源包括：PC机一台；软件资源：VS code、SQL sever等；现有技术人员的技术水平和已有的工作基础：已经修得面对对象程序设计、数据结构、软件工程、web信息管理系统学分，完成了相应实验与课程设计。依据现有的技术资源，项目能够实现。

经济可行性：

进行开发成本仅有开发人员的开发时间一项，软件基本都可用社区版平替，硬件仅使用一台PC机即可。在低成本的前提下，本项目带来的效益是远高于成本的。

社会可行性：

经评估与测定，项目并不存在任何侵犯、妨碍等责任问题，也不存在法律风险和社会负面影响；其运行方式在用户组织内完全可行；与现有管理制度、人员素质和操作方式也无任何冲突。

# 二 校内组队记账软件总体设计

## **（一）架构设计**

本系统是网络版软件【基于C/S架构】。主要优势在于：由于客户端实现与服务器的直接相连，没有中间环节，因此响应速度快。操作界面简洁、形式多样，可以充分满足客户自身的个性化要求。C/S结构的管理信息系统具有较强的事务处理能力，能实现复杂的业务流程。

**（二）功能设计**

经过上述需求分析，校内组队记账软件系统的功能可分为用户管理、队伍管理、队内操作、在线帮助，具体如表1所示。

表1 校内组队记账软件系统功能表

| 一级功能 | 二级子功能   | 功能详述                                           |
|----------|--------------|----------------------------------------------------|
|          | 用户登录     | 输入用户用户名和密码登录                           |
|          | 用户退出     | 退出用户账户                                       |
| 用户管理 | 用户添加     | 添加一名用户，包含各种信息                         |
|          | 用户删除     | 删除一名用户的各种信息                             |
|          | 修改用户信息 | 修改用户的信息                                     |
|          | 移除组内用户 | 从组内移除一名用户，包含其在组内进行过的借贷记录   |
|          | 查询校内学生 | 可用工号、寝室号等查询，也可在列表中查阅           |
| 队伍管理 | 创建队伍     | 创建一支自己在内的队伍                             |
|          | 查询队伍     | 可用队号等查询，也可在列表中查阅                   |
|          | 查看队伍成员 | 可以查看所有队伍的成员                             |
|          | 加入队伍     | 选择队伍后加入                                     |
|          | 删除队伍     | 删除队伍信息，同时删除队内成员的加入记录和记账记录 |
|          | 拉进新成员   | 将不在队伍中的人拉进队伍中                         |
| 队内操作 | 作为借方记账 | 将给队内某个成员从自己这里借出的金额记录在账上     |
|          | 查询组内账单 | 可以用几种属性分别查询账单                         |
|          | 在队伍里结算 | 结算出目前各个成员的赊欠与借出情况                 |
|          | 清除组内记录 | 将某条错误的记录删去                               |
| 在线帮助 | 在线帮助     | 在使用文档里查看使用方法                           |

## **（三）角色设计**

系统有两种种角色，分别是用户、管理员。

用户的功能有：用户登录、用户退出、查询校内学生、创建队伍、查询队伍、查看队伍成员、加入队伍、拉进新成员、作为借方记账、查询组内账单、在队伍内结算、清除组内记录；

管理员的功能有：用户登录、用户退出、用户添加、用户删除、修改用户信息、移除组内用户、查询校内学生、创建队伍查询队伍、查看队伍成员、删除队伍。

## **（四）开发和运行平台选择**

**⑴ 软件开发平台**

① 软件开发语言

本软件系统选用C\#语言作为开发语言。介C\#是微软公司发布的一种由C和C++衍生出来的面向对象的编程语言、运行于.NET Framework和.NET Core(完全开源，跨平台)之上的高级程序设计语言。C\#是由C和C++衍生出来的一种安全的、稳定的、简单的、优雅的面向对象编程语言。它在继承C和C++强大功能的同时去掉了一些它们的复杂特性（例如没有宏以及不允许多重继承）。C\#综合了VB简单的可视化操作和C++的高运行效率，以其强大的操作能力、优雅的语法风格、创新的语言特性和便捷的面向组件编程的支持成为.NET开发的首选语言。

② 软件开发工具

本软件系统选用Visual Studio作为开发工具。VS是一个基本[完整](https://baike.baidu.com/item/%E5%AE%8C%E6%95%B4/32785)的开发工具集，它包括了整个[软件生命周期](https://baike.baidu.com/item/%E8%BD%AF%E4%BB%B6%E7%94%9F%E5%91%BD%E5%91%A8%E6%9C%9F/861455)中所需要的大部分工具，支持 C\#、C++、TypeScipt/JavaScript 或 XAML 的任意工作负载一起安装。VS创建应用程序一般包括的步骤有：应用程序开发、创建应用程序用户界面、设置用户界面对象的属性、编写代码实现程序功能、测试和调试程序等。

③ 数据库管理系统

本软件系统选用SQL Server 2018作为数据库管理系统。SQL语言的主要功能就是同各种[数据库](https://baike.baidu.com/item/%E6%95%B0%E6%8D%AE%E5%BA%93/103728)建立联系，进行沟通。SQL语句可以用来执行各种各样的操作，更新数据库中的数据，从数据库中提取数据等。SQL Server 是一个[关系数据库管理系统](https://baike.baidu.com/item/%E5%85%B3%E7%B3%BB%E6%95%B0%E6%8D%AE%E5%BA%93%E7%AE%A1%E7%90%86%E7%B3%BB%E7%BB%9F),其具有图形化用户界面，使用方便，有着丰富的编程接口工具，在Oracle提供数据仓库功能，支持客户/服务器结构，具备分布式数据库功能。

利用SQL Server 可以对数据进行存储等管理，个人版适用于移动用户，单机数据库的支持。众所周知，SQL Server能够满足今天的商业环境要求不同类型的数据库解决方案。它一种应用广泛的数据库管理系统，具有许多显著的优点：易用性、适合分布式组织的可伸缩性、用于决策支持的数据仓库功能、与许多其他服务器软件紧密关联的集成性、良好的性价比等。性能、可伸缩性及可靠性是基本要求，而进入市场时间也非常关键。

**⑵ 软件运行平台**

① 硬件

本软件系统运行的最低硬件配置要求为：

处理器：Intel Core 2 Quad CPU Q6600 @ 2.40GHz (4 CPUs) / AMD Phenom 9850 Quad-Core Processor (4 CPUs) @ 2.5GHz 以上级别；

内存：4 GB RAM 及以上；

图形：NVIDIA 9800 GT 1GB / AMD HD 4870 1GB (DX 10、10.1、11) 以上级别。

② 软件

本软件系统运行的推荐操作系统为：Windows 10 64 Bit / 32 Bit及以上，macOS Catalina及以上，iOS / iPadOS 14 及以上。

## **（五）数据库设计**

本系统的数据库设计如下：

**⑴ 概念设计**

系统概念设计描述，本系统共有三个实体。管理员实体具有两个属性；学生实体具有四个属性；队伍实体共有三个属性；由于学生实体之间、学生与队之间是多对多的关系，故将二者联系转换为一个独立的关系模式,系统ER图如图1所示。

图1 组队记账系统ER图设计

**⑵ 逻辑设计**

本系统共设计了五张表：管理员表，学生表，队伍表，加入队伍表，记账表，个人借贷表；每个表都满足第三范式，具体如下：

① 管理员

管理员（账户，密码），主键：账户名；

② 学生

学生（学号，密码，姓名，寝室号），主键：学号；

③ 队伍

队伍（队号，队名），主键：队号；

④ 加入队伍

加入队伍（序号，学号，姓名，队号，队名，加入时间，累计赊欠金额，累计借出金额，结算时应支付/收款），主键：次序；

⑤ 记账

记账（序号，队号，队名，贷方学号，贷方姓名，借方学号，借方姓名，金额，时间，备注），主键：次序。

**⑶ 物理实现**

根据上述设计结果并结合本系统选择的数据库管理系统SQL sever，在SQL sever中创建五个表，如图2所示。

![](media/679a8eaf52c33c3395d11666ecaf9cb5.png)

图2 本软件数据库在XXX中的实现

① 管理员表

管理员表储存了管理员的登录账号，登录密码字段。管理员表的物理实现，如图3所示。

![](media/8af4961b1a2d649fa814ed4af5454956.png)

图3 管理员表在SQL sever中的实现

② 学生表

学生表储存了学生的学号，密码，姓名，寝室号字段。学生表的物理实现，如图4所示。

![](media/dedcf31fe0725c90e5658f68fdc0d786.png)

图4 学生表在SQL sever中的实现

③ 队伍表

队伍表储存了队伍的队号，队名字段。队伍表的物理实现，如图5所示。

![](media/d26fdeeef5ec56ebb574cdea22689863.png)

图5 队伍表在SQL sever中的实现

④ 加入队伍表

加入队伍报表储存了队伍的次序，学号，姓名，队号，队名，加入时间，累计赊欠金额，累计借出金额，结算时应支付/收款字段。加入队伍表的物理实现如图6所示。

![](media/2e5eb97c5821cdb73801c5349237da4d.png)

图6 加入队伍表在SQL sever中的实现

⑤ 记账表

记账表储存了账单的序号，队号，队名，贷方学号，贷方姓名，借方学号，借方姓名，金额，时间，备注字段。加入记账表的物理实现如图7所示.

![](media/76a5d6f04d6e1cf2e45d12c7a682580a.png)

图7 记账表在SQL sever中的实现

# 三 校内组队记账软件实现

## **（一）用户管理模块**

用户管理模块主要是用来管理以用户为单位的信息。其下的二级子功能有：用户登录、用户退出、用户添加、用户删除、修改用户信息、移除组内用户、查询校内学生。

**⑴ 用户登录子模块**

校内学生如果想要使用记账系统，就必须先进行登录，其账号信息已被提前导入系统。登录成功后，学生即可获得更多的操作权限。

① 界面设计

用户注册界面如图8所示。

![](media/eebf97a605aa12e7fc56a1c3363584ea.png)

图8 用户登录界面

页面中用到的控件有：label、textbox、radiobutton、button。

其中两个radiobutton用来选择登录身份，在第一个radiobutton的属性栏里，将checked一栏的属性从false改为true，即为在初始用户还未点击时，就选择“用户”的按钮。具体如图9所示。

![](media/fb934c59dc1cd88d20b7c5a45a2e82ab.png)

图9 radiobutton的checked属性栏设置

② 逻辑设计

用户注册的关键流程图如图10所示。

![](media/8452c7ba3a9e9f88cbf8acf839cd78a0.png)

图10 用户登录流程

③ 关键实现

该功能的实现，主要是在该页面类下面定义了一个Login方法，用来获取用户在文本框输入的账户名和账户密码并尝试匹配数据库内信息。所谓匹配即使用“select”语句在数据库内搜索。

将SQL语句传向SQL sever的实现，则是在之前就定义好的一个类：Dao，其下有五个public方法分别用来：连接数据库、封装传输SQL语句、执行语句并返回数据库里改变的行数、读取搜索到的数据、关闭与数据库的连接。由此，便可实现由C\#代码向数据库的连接。

将Login方法在“登录”button的click方法中调用，即可实现点击登录按钮进行登录的功能。

若登录成功，则将用户的姓名和学号保存在一个Data类中，以便后续使用时不再从数据库中获取。

**⑵ 用户退出子模块**

① 界面设计

在登录成功后，若想要退出到登录界面，只需点击右上角“×”按钮即可。如图11所示。

![](media/5d8d6d4fc2d79facd70776a51027890f.png)

图11 退出按钮

本页面用到的主要控件有：menuStrip、label；其中最后一个label的text属性一栏设置为“NULL”以便在代码部分实现显示用户名的功能。

② 逻辑设计

退出功能的逻辑设计如图12所示。

**![](media/1a3dda4c9d2e0007afafa5cd370c8c68.png)**

图12 用户退出的流程

③ 关键实现

在登录页面向用户操作页面转换时，在实例化用户操作页面之后，使用this.Hide()方法，隐藏当前登录页面，再使用user.ShowDialog()显示用户使用窗口，紧跟着使用this.Show()方法。即可达到效果：在登录成功后隐藏登录页面，关闭用户操作页面之后，返回到登录页面。

**⑶ 用户添加子模块**

① 界面设计

管理员登录之后，点击“学生列表”菜单栏里的“查看学生列表”即可进入到学生账户管理页面。在学生账户管理页面点击“添加账户”按钮，即可进入添加学生账户页面。页面设计如图13所示。

![](media/2fa3aae596d89a6588793f9d7a3db69f.png)

图13 用户添加子模块页面设计

本页面用到的主要控件有：textbox、label、button；其中在“确认添加”button的click方法的最后加入赋值语句textBox1.Text = "";将之前每个文本框输入过的值都清空，以便下次输入。该语句在后有文本框输入的页面都需添加，后文中不再赘述。

② 逻辑设计

用户添加功能的逻辑流程图如图14所示。

**![](media/6d381d9d6c2ce2dad7fbc432914de4b1.png)**

图14 用户添加功能的逻辑流程图

③ 关键实现

本功能的主要实现，是在“确认添加”button的click方法里，首先判断四个textbox里是否都有输入字段。若都有，将四个textbox获取到的字段，用“insert”SQL语句添加到数据库中的学生表中，同样也是用Dao方法实现连接。最后用Dao中的Execute（）方法执行语句并返回被影响的行数，若是返回的值大于0，则表明添加成功。显示弹窗“添加成功！”；否则显示弹窗“添加失败！”。

若有textbox的输入为空，则弹出弹窗“请完整输入各项信息！”。

**⑷ 用户删除子模块**

① 界面设计

在管理员登录之后的页面里，点击“学生列表”菜单栏里的“查看学生列表”即可进入到学生账户管理页面。其页面设计如图15所示。

**![](media/fff8bda280815400ad56a2a7b0ea3617.png)**

图14 学生账户管理页面

本页面用到的主要控件有：label、textbox、button、datagridview；其中datagridview需要手动设置列的数目和名称，其次还需要调整以下属性：允许用户增加和删除行的属性需改成false，如图15所示；

**![](media/47f36c49b686e7689853fa79afc127f8.png)**

图15 图中粗体的属性栏即刚修改过的样子

将multselect属性栏修改为false，意为限制用户一次只能选择一行而非多行。该设置在本软件中极为必要，因为包括本表格在内的多个表格都需要对表格中选中的对象为单位进行操作，如图16所示；

![](media/a8cf253e5268f1dabb59ba7bda9dae46.png)

图16 图中粗体的属性栏即刚修改过的样子

将rowheadersvisible设置为false，以取消默认表格中最前的不显示数据的一列，如图17所示；

![](media/001800dd0537b9fe4469d89b45ecd70d.png)

图16 图中粗体的属性栏即刚修改过的样子

将autosizecolumnsmode调整为Fill，则已添加的列将自适应充满表格的大小，如图17所示；

![](media/fae475e1f67fa35ef790100fc2025e06.png)

图17 图中粗体的属性栏即刚修改过的样子

将selectionmode属性栏选择为fullrowselect，意为选择表格里的对象时，一次选择一行，如图18所示；

![](media/b4084ad2f0aa11e1847ca72cff6ef6a1.png)

图18 图中粗体的属性栏即刚修改过的样子

将Dock属性栏选择为Left，即为表格控件的位置为贴着页框的左边，如图19所示。

![](media/993a4f9cfba8bb800447e444ee70c9f7.png)

图19 图中粗体的属性栏即刚修改过的样子

页面设计里带有表格的页面都进行类似的设置，后文中不再赘述。

② 逻辑设计

用户删除子模块的关键流程图如图20所示。

**![](media/9ae77a4ddf2622e8ee7eef921eb9efd8.png)**

图20 用户删除功能的的流程图

③ 关键实现

首先在该页面类下定义一个public方法，名为Table，起作用为从数据库读取数据显示在表格控件中。该方法实例化Dao类来执行一个“select”语句，将表格需要的数据从数据库中读到本页面的表格中。该方法还可被调用，当表格需要刷新的时候。页面设计里带有表格的页面都会定义一个Table方法，其具体代码因表格环境而略有差异，但其思想和功能大致相同，后文中不再赘述。

在“删除用户”button的click方法里，首先定义一个string类型变量，用来获取当前选中用户的学号，按下“删除用户”的button之后，显出弹窗“确认删除吗？”。选“是”之后，用dao类将删除语句封装执行，返回受影响的行数。若返回值大于0，则显示弹窗“删除成功”。否则显示弹窗“删除失败”。

**⑸ 修改用户信息子模块**

① 界面设计

管理员登录之后，点击“学生列表”菜单栏里的“查看学生列表”即可进入到学生账户管理页面。在学生账户管理页面点击“修改账户信息”按钮，即可进入修改账户信息页面。页面设计如图21。

**![](media/51361f1952d5867397419fda9d61bee6.png)**

图21 修改账户信息页面

本页面用到的主要控件有：textbox、label、button；其中在“确认修改”button的click方法的最后加入赋值语句textBox1.Text = "";将之前每个文本框输入过的值都清空，以便下次输入。

② 逻辑设计

该模块的主要流程如图22所示。

**![](media/7286baf3d3e461989e1155b47d120590.png)**

图22 修改学生信息的主要流程图

③ 关键实现

首先，在修改账户页面类中，添加一个同名构造函数，其包含一个string类型的参数。这样，在前一个页面类中实例化该页面时，就可以用这个参数的位置将已选中的学生的学号传递到该页面的类中，以便对该条信息进行修改。之后执行“update”语句，用之前的方法完成修改学生信息的功能。

**⑹ 移除组内用户子模块**

① 界面设计

管理员登录系统之后，在队伍列表菜单栏里选择查看队伍列表，即可进入队伍管理页面，如图23。

**![](media/3be277e2a57e735689fd251984a09592.png)**

图23 队伍管理页面

点击“查看队伍成员”进入队内成员管理页面，如图24。

![](media/684ff4b3d5acb70db197bc2875db5cba.png)

图24 队内成员管理页面

本页面用到的主要控件有：label、textbox、button、datagridview；其中datagridview需要手动设置列的数目和名称，其次还需要调整一些属性，大致与之前页面的设置相同。

② 逻辑设计

本模块的逻辑流程图如图25所示。

![](media/8041f37c93e951a63053248521875195.png)

图25 移除队内成员的逻辑流程图

③ 关键实现

该模块的功能都在“确认删除”button的click方法里实现。首先依旧定义一个string类型变量，用来获取表格中已选那行的学号，之后用dao类实现“delete”语句的执行，最后返回被影响的行数以判断是否移除成功。

**⑻ 查询校内学生子模块**

① 界面设计

在管理员登录之后的页面里，点击“学生列表”菜单栏里的“查看学生列表”即可进入到学生账户管理页面。其页面设计如图26所示。

**![](media/9b01e3ff4b2e79a988b7fe2cce9f2049.png)**

图26 学生账户管理页面

学生用户在进入自己加入队内之后，点击“拉进新成员”按钮，即可看到学生列表。如图27所示。

**![](media/044aece8ed5cbaeff603066a3b5e5068.png)**

图27 用户拉人进队页面

本页面用到的主要控件有：label、textbox、button、datagridview。

② 逻辑设计

查询校内学生的逻辑流程图如图28所示。

**![](media/aac1d2db691125d04d3580c6abfba4fd.png)**

图28 用户查询子功能流程图

③ 关键实现

该功能的实现，是在具有该功能的页面类下面，定义查询方法，再在button的click方法下调用相应查询方法。学号查询方法，主要是定义string获取文本框的字段，实例化dao类，用“select”语句查询之后，在显示在文本框中。寝室号查询基本相同，在学号查询的基础上，对SQL语句加入了模糊查询。

## **（二）队伍管理管理模块**

**⑴ 创建队伍子模块**

① 界面设计

管理员登录系统之后，在队伍列表菜单栏里选择查看队伍列表，即可进入队伍管理页面，点击“添加队伍”按钮进入添加队伍页面，如图29所示。

**![](media/e8dbf4fbdd9c27154d07c41eff5dd165.png)**

图29 添加队伍页面

用户登录成功之后，点击创建队伍菜单栏，即可进入用户创建队伍页面。如图30所示。

**![](media/8644b5b625342926abb8262aaedfdc1c.png)**

图30 用户创建队伍页面

以上两个页面包含的控件有：label、textbox、button。

② 关键实现

管理员添加队伍的实现方法与添加用户大致相同，实例化dao类来执行SQL语句。

用户创建队伍时，默认将自己加入队伍，故在“确认创建”button的click方法中额外执行一句将自己加入刚创建好的队伍的SQL语句。

**⑵ 查询队伍子模块**

① 界面设计

管理员登录之后，在队伍列表菜单栏里点击查看队伍列表，即可进入队伍管理界面，在此即可查询队伍，如图31所示。

**![](media/3dbf2b028ff8cf017cda7746ba8623c6.png)**

图31 队伍管理页面

用户登录之后，点击加入已有队伍菜单栏，即可进入用户查看已有队伍界面，在此也可查询队伍，如图32所示。

**![](media/2216974a3cbf0f72c4ed3d40a18e4784.png)**

图32 用户查看已有队伍页面

本页面用到的主要控件有：label、textbox、button、datagridview。

② 逻辑设计

查询队伍子功能的逻辑流程图如图33所示。

**![](media/6c9d7ed9fb4a514bf6f6a0129e7ef91d.png)**

图33 查询队伍功能的逻辑流程图

③ 关键实现

该功能的实现与上文中提到的查询学生的实现大致相同。在具有该功能的页面类下面，定义查询方法，再在button的click方法下调用相应查询方法。队号查询方法，主要是定义string获取文本框的字段，实例化dao类，用“select”语句查询之后，在显示在文本框中。队名查询基本相同，在队号查询的基础上，对SQL语句加入了模糊查询。

**⑶ 查看队伍成员子模块**

① 界面设计

用户登录后，点击加入已有队伍菜单栏，打开用户查看已有队伍页面，选择队伍之后，点击“查看队伍成员列表”以查看队伍成员，如图34所示。

**![](media/a0d419089fcfa304a7edf046ee675669.png)**

图34 用户查看队伍成员列表

该模块仅仅用到datagridview控件，并进行了上文中提到的属性设置。

② 关键实现

该功能的实现，同样用到了编写含参构造函数传参的方法，将队号由上一个页面传到了用户查看队伍成员列表页面。该表格中信息的获取同样使用了Table（）方法。

**⑷ 加入队伍子模块**

① 界面设计

用户登录后，点击加入已有队伍菜单栏，打开用户查看已有队伍页面，可在该页面下选择队伍加入，如图35所示。

**![](media/2216974a3cbf0f72c4ed3d40a18e4784.png)**

图35 用户查看已有队伍页面

② 逻辑设计

该模块的逻辑流程图如图36所示。

**![](media/a753c0699406e177505f1b044be63662.png)**

图36 加入队伍的逻辑流程图

③ 关键实现

在“加入这支队伍”的click方法中，实例化dao类来实现“insert”SQL语句，将该用户添加到该队伍的加入表中。需注意的是，此处不需要再从表中或上个页面获取用户的学号，因为在登录时用户学号和姓名已被存入到data类中，直接获取即可。

**⑸ 删除队伍模块**

① 界面设计

管理员登录之后，在队伍列表菜单栏里点击查看队伍列表，即可进入队伍管理界面，在此即可查询队伍，如图37所示。

**![](media/3dbf2b028ff8cf017cda7746ba8623c6.png)**

图37 队伍管理页面

② 逻辑设计

该模块的逻辑流程图如图38所示。

**![](media/83df0d6752e16b6c05c60c7ee73e4818.png)**

图38 删除队伍子模块的逻辑流程图

③ 关键实现

该模块的功能与之前的删除功能类似，都在“确认删除”button的click方法里实现。首先依旧定义一个string类型变量，用来获取表格中已选那行的学号，之后用dao类实现“delete”语句的执行，最后返回被影响的行数以判断是否删除成功。

## **（三）队内操作模块**

**⑴ 拉进新成员子模块**

① 界面设计

用户在登录之后，点击“我的队伍”菜单栏，在“我的队伍界面”选择一支队伍，点击“在队内进行记账等操作”，进入队内操作界面，在该界面内点击“拉进新成员”即可进入用户拉人界面，界面设计如图39所示。

**![](media/c1e21975bf66f0595a5a8a98e5076ac1.png)**

图39 用户拉人界面

② 逻辑设计

拉进新成员子模块的逻辑流程图如图40所示。

**![](media/2f49659bf2580fc5e488389d737c1eae.png)**

图40 拉进新成员的逻辑流程图

③ 关键实现

首先用同名构造函数传递队伍号到用户拉人页面的类，然后定义string类变量获取在表格中选中的学生学号，最后实例化dao类执行“insert”SQL语句实现将学生添加到队伍中的目的。

**⑵ 作为借方记账子模块**

① 界面设计

用户在登录之后，点击“我的队伍”菜单栏，在“我的队伍界面”选择一支队伍，点击“在队内进行记账等操作”，进入队内操作界面，在该界面内点击“作为借方队该成员进行记账”即可进入记账界面，界面设计如图41所示。

**![](media/774a9f3ac0267822b85b3a002092bb70.png)**

图41 记账界面

② 逻辑设计

记账功能的逻辑流程图如图42所示。

**![](media/d9371f73791a5ef842de2a9cd03c2d4e.png)**

图42 记账功能的逻辑流程图

③ 关键实现

先使用同名构造函数的方法，将队号与贷方学号都传到记账页面的类里，由于借方就是此时登录使用系统的账户，故其信息可从data类中获取。在执行SQL语句时，除了向记账表中记录一条借账记录，还要分别向借方和贷方的加入队表中的borrowmoney、lendmoney中加上这次记账的金额；finalmoney字段中，减去或加上这次借账的金额。这样，borrowmoney就代表该用户累计赊欠的金额；lendmoney就代表该用户累计借出的金额；finalmoney就代表着该用户在这个队伍中收支相抵之后的借贷金额，这主要是为了使结算时信息更加清晰。

**⑶ 查询组内账单子模块**

① 界面设计

用户在登录之后，点击“我的队伍”菜单栏，在“我的队伍界面”选择一支队伍，点击“在队内进行记账等操作”，进入队内操作界面，在该界面内点击“查看组内账单并操作”即可进入查看组内账单界面，界面设计如图43所示。

**![](media/5bc40be0db51715ff2637d55941ebeff.png)**

图43 查看组内账单并操作界面

② 关键实现

首先用包含string类型参数的同名构造函数传队号到该页面的类中，之后用Table（）方法从数据库记账表中获取该队的所有记账记录并写入到表格中。

定义查询方法，再在button的click方法下调用相应查询方法。金额和序号查询方法，主要是定义string获取文本框的字段，实例化dao类，用“select”语句查询之后，在显示在文本框中。备注和时间查询基本相同，在此前的基础上，对SQL语句加入了模糊查询。

**⑷ 在队内结算子模块**

① 界面设计

用户在登录之后，点击“我的队伍”菜单栏，在“我的队伍界面”选择一支队伍，点击“在队内进行记账等操作”，进入队内操作界面，在该界面内点击“查看组内账单并操作”即可进入查看组内账单界面，点击“全部结算”即可进入队内结算页面，界面设计如图44所示。

**![](media/ab97403c8dc51545a0100678da068f04.png)**

图44 队内结算页面

② 关键实现

首先用包含string类型参数的同名构造函数传队号到该页面的类中，之后用Table（）方法从数据库加入表中获取该队的所有成员记录，仅获取表中所示的五行并写入到表格中。注意此处获取的记录正是上文中提到的记录在加入队伍表中的borrowmoney、lendmoney和finalmoney。

**⑸ 创建队伍子模块**

① 界面设计

用户在登录之后，点击“我的队伍”菜单栏，在“我的队伍界面”选择一支队伍，点击“在队内进行记账等操作”，进入队内操作界面，在该界面内点击“查看组内账单并操作”即可进入查看组内账单界面，此界面内即可进行借账记录的删除，界面设计如图44所示。

**![](media/5bc40be0db51715ff2637d55941ebeff.png)**

图44 查看组内账单并操作界面

② 关键实现

在“删除该条记录”button的click方法里，首先定义一个string类型变量，用来获取当前选中用户的学号，按下“删除用户”的button之后，显出弹窗“确认删除吗？”。选“是”之后，用dao类将删除语句封装执行，返回受影响的行数。若返回值大于0，则显示弹窗“删除成功”。否则显示弹窗“删除失败”。

## **（三）在线帮助模块**

**⑴ 在线帮助子模块**

① 界面设计

用户在登录之后，用户使用界面的菜单栏里点击帮助，则会显示用户在线帮助页面。如图45所示 。管理员在管理员主页面菜单栏中点击帮助之后，则会显示管理员在线操作主页面。如图46所示。

**![](media/cad54e802c9024a5588e76c104a5888d.png)**

图45 用户在线帮助页面

**![](media/27f9c248b88163abd20c63fa638980a5.png)**

图46 管理员在线帮助页面

② 关键实现

本功能实现较为简单，在用户使用界面和管理员使用界面的帮助菜单栏click方法下实例化在线帮助页面，在在线帮助页面内安放数个label即可。

# 四 校内组队记账软件测试

## **（一）用户管理**

**⑴ 用户登录**

管理员和用户在使用本系统之前都需要进行登录，管理员和用户的登录信息都已被提前导入到后台数据库中无需注册。当登录者输入正确的账户名和密码，并选择对身份之后，点击登录按钮，即会弹出弹窗：“登录成功！”。如图47所示。

![](media/accdc215468ea7ecb32044a6bcab4728.png)

图47 登录成功

若是输入了错误的账户或密码，或是对于管理员和用户的身份选择错误，则在后台数据库文件中匹配不到相应的数据，就会出现弹窗“登录失败！”。如图48所示。

![](media/9b7c04e8c2fc4ded512a384695ba8e36.png)

图48 登录失败

若是的账户和密码的对应文本框内没有输入信息，或者输入了一项信息，点击登录按钮后则会显示弹窗“输入不得为空！”。如图49所示。

![](media/35c6109618e0b6f63d8f2c0247e7af08.png)

图49 输入不得为空

**⑵ 用户登录**

在已登录的页面下，若是管理员或用户想退出该页面重新登录，则点击右上角的关闭按钮即可退出到登录页面。如图50所示。

**![](media/a66cee7ef8f2e8709151074a20269793.png)**

图50 退出登录

**⑶ 用户添加**

在管理员已登录页面，点击菜单栏里的学生列表，随后点击查看学生列表，即可进入学生账户管理页面，如图51和图52所示。

**![](media/a72489b330f49ddc30f6edefb40cd674.png)**

图51 查看学生列表

**![](media/82a8ad8dd6ed58a5b6b2016668652152.png)**

图52 学生账户管理页面

在学生账户管理页面下，点击添加账户按钮，即可进入添加学生账户页面。在该页面内的学号，姓名，密码，寝室号相应的文本框内输入对应的信息，点击确认添加按钮。则会成功添加该学生的信息，显示“添加成功！”弹窗。如图53所示。

**![](media/45d2f0657ba6f7a4936ab9f4bf4dd1db.png)**

图53 添加成功

点击确定后，刚刚输入文本框内的字段则会被清除，以便下一次输入。若是文本框内的信息没有被输入全就按下确定添加按钮，则会显示弹框“请完整输入各项信息！”。如图54所示。

**![](media/8c659cc41706df12ad4e53d2c46a9745.png)**

图54 请完整输入各项信息

关闭添加学生账户页面之后，学生账户管理页面的信息表格会自动刷新，将刚刚新添加的账户显示在表格上面。如图55所示。

**![](media/9e6a30874afad5b649295f2218b43f53.png)**

图55 显示刚刚添加的学生账户信息

**⑷ 用户删除**

在学生账户管理页面下，选中表格内的学生账户，右上角会有两个文本框，显示现在选中的学生学号和姓名，以便管理员确认。如图56所示。

**![](media/dd0d01d5aac2194e447f5dcd28374ca8.png)**

图56 选中学生的学号和姓名

点击删除账户按钮则会显示信息提示弹窗“确认删除吗”。如图57所示。

**![](media/884525404126d79e80e23d1328293558.png)**

图56 确认删除信息提示弹窗

点击确定后显示弹窗“删除成功！”。确认该弹窗之后，学生账户管理页面的表格再次自动刷新。刚刚删除的账户不会出现在该表格中，如图57所示。

**![](media/3530e198ad4e2979378c4e8d976195e6.png)**

图57 删除成功

**⑸ 修改用户信息**

在学生账户管理页面下点击修改用户信息按钮，则会进入修改用户信息页面。如图58所示。

**![](media/2aa3b3f9e4a66019e9bf9d44947528b2.png)**

图58 修改用户信息页面

在该页面下修改一项或多项信息后，点击“确认修改“按钮，则会弹出“修改成功“弹框。如图59所示。

**![](media/303526d65053d92d53949195eaf64626.png)**

图59 修改成功

**⑹ 查询校内学生**

使用学号查询时，在学号查询按钮对应的文本框内输入想要查询的学生学号，按下学号查询按钮即可在左边表格里显示出该学号对应的学生信息。如图60所示。

**![](media/a9da97559665d599d01f21256ed02ab5.png)**

图60 学号查询

按下“刷新列表”按钮，即可重新获取所有学生的信息。使用寝室后查询时，在寝室后查询对应的文本框内输入想要查询的寝室号。按下“寝室号查询”按钮即可查询出对应寝室号的学生信息。如图61所示。

**![](media/766c3ac9c0fdf0476afb4f2fbcedebdd.png)**

图61 寝室号查询

此外，寝室号查询还支持模糊查询的功能。例如，只知道寝室门牌号的情况下，输入寝室门牌号，就可以得到相关的内容。如图62所示。

![](media/a7dfab8eb15df31945023495357ae888.png)

图62 寝室号模糊查询

**⑺ 移除组内用户**

在管理员主页面中点击队伍列表，菜单栏选择查看队伍列表，进入队伍管理页面。如图63和64所示。

![](media/84a6c69247ba67e62b8e78f368e5daa4.png)

图63 查看队伍列表

![](media/113353122a4c9a081c9b86ac8de7ad3b.png)

图64 队伍管理页面

在选择好队伍之后，点击查看队伍成员按钮，进入队内成员管理页面，选择一名队员，并点击移出队伍按钮，则会显示信息提示弹框“确认删除吗？”。点击确定则会弹出删除“成功弹窗”。如图65和66所示。

![](media/f0afd2c9be6b89ba845f2b5395c73040.png)

图65 确认删除弹窗

**![](media/3530e198ad4e2979378c4e8d976195e6.png)**

图66 删除成功

## **（二）队伍管理**

**⑴ 创建队伍**

管理员与用户都可创建队伍，其过程大致相同。唯一差别是用户创建完队伍之后，会自动将自己加入到新创建的队伍中。但在操作界面里不体现。故此处以用户创建队伍为例做演示。

首先在用户使用界面点击菜单栏创建队伍。如图67所示。

**![](media/d3d672c5e000a698b6325b80a35a5cb2.png)**

图67 创建队伍

在弹出的用户创建队伍页面里输入队名。点击确认创建，显示创建成功弹窗即表示创建成功。如图68所示。

**![](media/1136da29f57e2b2fbcfe9f867577e858.png)**

图68 用户创建队伍页面

接着会显示弹窗，已将自己加入队伍中。表示创建该队伍的用户已被加入到队伍中。如图69所示。

**![](media/8a8e22e87daf411f57eb09774fb0eec5.png)**

图68 加入队伍

**⑵ 查询队伍**

管理员与用户都可进行查询队伍的操作，其过程大致相同。此处以用户为例作为展示。在用户使用界面点击菜单栏加入已有队伍。如图69所示。

**![](media/a4812f2126293cad7c072aca2bec85c3.png)**

图69 加入已有队伍菜单栏

进入用户查看已有队伍界面之后，即可进行队伍查询的功能。与邵文中管理员查询用户功能类似，队号查询为精确查询，队名查询为模糊查询。如图70和图71所示。

**![](media/ed0c6e7788dbf62a60fdbaa24736cb9e.png)**

图70 队号查询

**![](media/a4f80ddc434dd495d932dcf9c2dfd548.png)**

图71 队名模糊查询

**⑶ 查看队伍成员**

查看队伍成员也是用户与管理员即可执行的功能，管理员的相关演示已包含在上文“移除组内用户”的功能中，以下演示用户查看队内成员的操作。

在用户查看已有队伍页面中，选择一支队伍，点击查看队伍成员按钮，即可弹出用户查看对内成员页面。如图72所示。

**![](media/8580da7eb59e32d15805a2337f73d5ac.png)**

图72 用户查看队内成员页面

**⑷ 加入队伍**

在用户使用界面点击菜单栏加入已有队伍。如图73所示。

**![](media/a4812f2126293cad7c072aca2bec85c3.png)**

图73 加入已有队伍菜单栏

在进入用户查看已有队伍页面之后，便可使用加入队伍功能。在左侧的列表里选中一支队伍。点击加入这支队伍按钮，显示弹窗“已将自己加入队伍中！”。

![](media/dedafb8ee57cfcc091003c2ee035bf13.png)

图74 加入成功

**⑸ 删除队伍**

管理员在管理员主页面点击队伍列表菜单栏进入队伍管理页面之后，在表格里选择一支队伍，点击删除队伍按钮，会显示信息提示弹框确认删除吗，如图75所示。

**![](media/0ae0229510b36e65f0ca61d34ad4170a.png)**

图75 确认删除弹窗

点击确定之后，会显示弹框已删除该队伍。如图76所示。

**![](media/bc1525ff7453deac29de0cc7e35ce405.png)**

图76 成功删除队伍

若组内有成员，则会删除组内的成员加入信息与组内记账信息。若该组内没有组员，则会显示出弹框该组内没有可删除的成员信息，若干组内没有记账信息则会显示弹框。该组内没有可删除的记账信息，如图77和78所示。

**![](media/56248926082d217bdeaa613b50b07e56.png)**

图77 没有成员信息

**![](media/fe61d33c36e7531a9524638954cd58e4.png)**

图78 没有记账信息

## **（三）队内管理**

**⑴ 拉进新成员**

拉进新成员功能在队内操作页面里实现，在该页面内点击拉进新成员按钮，即可进入用户拉人界面。该界面内也可进行用户查找的操作，有时候查询学号和寝室的查询两种方式。选择一名同学，并点击下方拉进队伍按钮后，会显示弹窗“已将同学拉进队伍中！”，如图79所示。

**![](media/85320e781b6f2d70dd53fddb1255d1e7.png)**

图79 成功拉人入队

**⑵ 作为借方记账**

在队内操作页面，选中一位该队内的成员，点击作为借方对该成员进行操作，如图80所示。

**![](media/1565ad37457d1e83407bfa585f703b81.png)**

图80 队内操作界面

在记账页面下，输入金额和备注，点直接确认记账，显示弹窗记账成功，如图81所示。

**![](media/58e7399f60203859c4747f513021907d.png)**

图81 成功记账

**⑶ 查询组内账单**

在队内操作页面内，点击查看组内账单并操作按钮，即可进入查看及操作组内账单界面。共有四种查询账单的方法，分别是金额查询，时间查询，备注查询。序号查询。其中备注的时间都是模糊查询。图82到图85，别是四种查询方法的演示。

**![](media/0ccc7ace438d5c10efd6a784e0d41f47.png)**

图82 金额查询

**![](media/327a596404abb910820ac3052912416d.png)**

图83 备注查询

**![](media/ff20172905ed573b756aa96a014a90d1.png)**

图84 时间查询

**![](media/f414bbf2d1380c4eb5797653de5c7277.png)**

图85 序号查询

**⑷ 在队伍里结算**

在查看及操作对内账单页面里，点击全部结算按钮，则会显示队内结算页面,显示出当前所有组内用户共赊欠的金额、共借出的金额和结算时应支付或收款的金额。如图86所示。

**![](media/0bd40b6ce0aff10055a53240917319c2.png)**

图86 队内结算页面

**⑸ 在队内清除记录**

在查看及操作组内账单页面中，选择一条记账记录，点击删除该条记录按钮，出现信息提示弹窗“确认删除吗？”点击“确定”，出现“已删除该条记录!”弹窗。如图87和88所示。

**![](media/e61d9c02e0f3b64df38fa0cc40993fbc.png)**

图87 删除记录的提示弹窗

**![](media/6b5647ee11839c9e051e75f2ed688924.png)**

图88 成功删除

## **（四）在线帮助**

**⑴ 在线帮助**

用户在登录之后，用户使用界面的菜单栏里点击帮助，只会显示用户在线帮助页面。如图89所示 。管理员在管理员主页面菜单栏中点击帮助之后，则会显示管理员在线操作主页面。如图90所示。

**![](media/cad54e802c9024a5588e76c104a5888d.png)**

图89 用户在线帮助页面

**![](media/27f9c248b88163abd20c63fa638980a5.png)**

图88 管理员在线帮助页面

# 五 校内组队记账软件开发总结

## **（一）主要功能**

用户可使用该系统在本校范围内，自由选择未来会与自己产生借贷关系的一名或多名同学，进行组队关系，并在队内对成员进行记账。每当队内成员发生财物借贷时，借出者主动作为用户在系统上进行记账。本系统给予了用户丰富的视图，既可查阅整个小组内的账单，又可以针对小组内的成员个人，查阅其结账记录。

当队内成员多且借贷关系繁杂时，系统可以省去人工繁杂的计算，实时清算出每个成员收支相抵后应支出或收入的金额，以及在清算后向每位用户显示该偿还或亏欠的成员及金额。

管理员拥有一般用户的视图，即可以查看校内所有成员及已组成的队伍，并且拥有在初始用户列表里添加或删除用户账户的权限，还可以从已经成立的组内删除成员。

## **（二）主要用途**

本软件可用于记录学生群体之间的复杂借账关系，将传统的记账本电子化，使账单更加不易出错且免去繁杂的人工计算；借出方主动记账的设计也使得借出方更加主动，使碍于情面不便催账的情况不复存在。

## **（三）技术特点**

本软件各个功能的实现，本质上是对用户想要操作的数据进行增、删、改、查，

因此，与数据库的连接就尤为重要。本软件中将SQL语句传向SQL sever的实现，是在之前就定义好的一个类：Dao，其下有五个public方法分别用来：连接数据库、封装传输SQL语句、执行语句并返回数据库里改变的行数、读取搜索到的数据、关闭与数据库的连接。由此，便可实现由C\#代码向数据库的连接。

## **（四）下一步工作**

在本软件的功能设计中，原计划在队内结算的功能上，除了显示目前已有的共赊欠金额，共借出金额，结算时应支付或收款金额之外，还要显示出每个赊欠方应转账给借出方的金额及其转账的对象，以最少的转账次数完成队内成员的清算，即得到最优的转账方案。但该功能涉及算法相关的内容，后期时间仓促，没有达到理想的效果，遂取消。若之后有机会精进该软件，可将此列为改进的方向。
