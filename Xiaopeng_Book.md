## 一、路漫漫其修远兮，吾将上下而求索

NB666:掌握了别人可能就会对你说NB666的知识点！！！

励志写出最好的小鹏书

### 1. Hello,Qt

#### 1.1 Qt简介

```
C++是一种通用的标准化编程语言，使用任何编辑器都可以编写C++源程序，然后利用C++编译器对程序进行编译，就可以生成可执行的程序。
```

```
IDE介绍：
IDE实现目的：为了方便进行C++程序的编写和编译，有各种综合开发环境（Integrated Developing Environment,简称IDE）

常见的IDE:	
	Windows: Visual Studio
	
IDE功能：一个IDE不仅提供程序的编辑和编译，一般还提供一套基本类库，用于提供支持平台应用程序开发的各种基本类，如Visual Studio使用MFC进行Windows平台的应用程序开发
```

```
Qt发展史
第一阶段：挪威的Haavard Nord和Eirlk Chambe-Eng 在1991年开始开发，在1994年发布，并成立了一家名为Trolltech的公司
第二阶段：2008年诺基亚公司收购了Trolltech公司
第三阶段：2012年Digia公司收购了Qt
第四阶段；2014年成立了独立的Qt公司，专门进行Qt的开发，维护和商业推广
```

```
Qt现在的成就
经过20多年的发展，Qt已经成为了最优秀的跨平台开发框架之一，在各行各业的项目开发中得到广泛应用。
许多大型软件都是Qt开发的，如AutoDesk Maya、Google Earth、Skype、WPS Office等
```

```
C++Qt开发好处
C++语言使用广泛，长盛不衰，易在不同平台上移植，其编译生成的程序执行效率高，所以在专业研究领域很多开源的算法程序或类库都是用C++编写的。使用QtC++编写应用程序，可以使自己的应用程序具有跨平台移植的功能，也可以利用各种开源的类库资源。
```

```
Qt是一个跨平台的C++图形用户界面库，Qt的本质就是C++类库，使用Qt就是怎样使用Qt类库中的类及其类中的成员函数的问题。在Qt5中，QML(声明性语言)和Qt Quick成为Qt的核心之一，但C++仍是Qt的核心。Qt5的源代码文件必须使用UTF-8编码。
Qt虽然是使用的C++语言，但不是标准的C++，Qt进行了一定程度的拓展。
```



#### 1.2 Qt的获取与安装

##### 1.2.1 Qt的许可类型

```
Qt的许可类型：
	商业许可(购买商业许可需要支付费用)：
		允许开发者不公开项目的源码，其Qt版本包含更多的模块（某些模块只有商业许可的版本才有），并能获取Qt公司的支持。
	开源许可(购买开源许可不需要支付费用)：
		LGPLV3协议
		GPLV2/GPLV3协议
		
Qt的许可使用场景：
	开源许可：对于Qt的学习来说，初学Qt使用开源版本的软件即可
	商业许可：需要开发大型软件，并且不希望按照开源许可协议的要求公开源代码，以便对编写软件进行版权保护，则可以购买Qt的商业许可。
```

##### 1.2.2 Qt的版本

```
建议选用最新版本的Qt进行程序开发：
	Qt的版本更新比较快，且版本更新时会增加一些类或停止维护一些以前版本的类，例如Qt5与Qt4就有较大的区别，如果不是为了维护用旧版本编写的程序，一定要选用最新版本的Qt进行程序开发。
```

##### 1.2.3 Qt的下载与安装

```
根据开发项目不同，Qt分为“桌面和移动设备应用开发” 和 “嵌入式设备开发” 两大类不同的安装包
	桌面和移动设备应用开发：
		开发在PC、服务器、手机、平板电脑等设备上运行的程序，操作系统平台可以是Windows、Linux、macOS、Android等，用于桌面和移动设备应用开发的Qt具有开源许可协议，可以免费下载和使用。
	嵌入式设备开发：
		针对具体的嵌入式设备来开发应用程序，如物联网设备、汽车电子设备、医疗设备等特定的嵌入式设备。用于嵌入式设备开发的Qt可下载30天试用版本。
		
目前笔者（Gaopeng）所接触的是桌面应用程序开发的，所以下载的是桌面和移动设备开发的Qt开源版本，根据Qt官网的提示，注册用户后才可以下载Qt安装程序。

Qt的安装包分为在线安装包和离线安装包，为便于重复安装，最好下载离线安装包
	在线安装包
	离线安装包
		根据操作系统平台不同
			Linux版本
			macOS版本
			Windows版本
		根据使用的编译器不同（Qt5.9以前版本）
			MinGW 32-bit版本
			MSVC2015 32-bit版本
			MSVC2015 64-bit版本等

(NB666)安装过程中出现的安装模块选择：
Qt5.9.1
	Tools
√	MinGW 5.3.0 32bit	MinGW是Windows平台上使用的GNU工具集导入库的集合
×	UWP xxx1			用于UWP编译的模块
×	UWP xxx2
	...
×	msvc2013 64-bit	用于Windows平台上的MSVC编译器模块，要安装MSVC编译器模块，需要计算机安装相应版本的Visual Studio
×	msvc2015 32-bit
×	msvc2015 64-bit
×	msvc2017 64-bit
×	Android x86		用于安卓平台的模块
×	Android ARMv7
×	Sources			Qt的源码
√	Qt Charts		二维图表模块，用于绘制柱状图、饼图、曲线图等常用二维图表
√	Qt Data Visualization	三维数据图标模块，用于数据的三维显示
√	Qt Purchasing	
√	Qt Virtual Keyboard
√	Qt WebEngine
√	Qt NetWork Auth(TP)		 TP:表示技术预览
√	Qt Remote Objects(TP)	 TP:表示技术预览
√	Qt Speech(TP)			TP:表示技术预览
×	Qt Script(Deprecated)	 脚本模块	Deprecated:表示过时的模块
	...
Tools	工具软件
	Qt Creator 4.3.1
√	Qt Creator 4.3.1 CDB Debugg...	用于Qt程序开发的IDE
√	MinGW 5.3.0		MinGW工具链
×	Strawberry Perl 5.22.1.3	Perl语言工具

安装后的软件预览：
	Qt Creator 4.3.1(Community):它是用于开发Qt程序的IDE，是Qt的主要工具软件
	Tools:
		Assistant:是一个独立的查看Qt帮助文件的程序，集成在了Qt Creator中，即F1的帮助文件
		Designer:是一个独立的进行窗口、对话框等界面可视化设计的程序。Designer也集成在了Qt Creator中，在QtCreator中编辑或创建界面文件时，就可以自动打开并进行界面设计。即Ui绘制界面
		Linguist:是一个编辑语言资源文件的程序，在开发多语言界面的应用程序时会用到
	以上的3个工具软件可单独使用，前两个集成到了QtCreator里，可在Qt Creator打开，所以Qt的主要工具是QtCreator，要编写Qt程序，运行QtCreator即可。
```

#### 1.3 新建项目的GUI介绍

##### 1.3.1 新建一个项目

```
Qt Creator可以创建多种项目
	Qt Widgets Application:支持桌面平台的有图形用户界面(Graphic User Interface,GUI)界面的应用程序，GUI的设计完全基于C++语言，采用Qt提供的一套C++类库。
	Qt Console Application:控制台应用程序，无GUI界面，一般用于学习C/C++语言，只需要简单的输入输出操作时可创建此类项目。
	Qt Quick Application:创建可部署的Qt Quick2应用程序。Qt Quick是Qt支持的一套GUI开发架构，其界面设计采用QML语言，程序架构采用C++语言。利用Qt Quick可以设计非常炫的用户界面，一般用于移动设备或嵌入式设备上无边框的应用程序的设计。
	Qt Quick Controls 2 Application:创建基于Qt Quick Controls 2组件的可部署的Qt Quick2应用程序。Qt Quick Controls2组件只有Qt5.7及以后版本才有。
	Qt Canvas 3D Application:创建Qt Canvas 3D QML项目，也是基于QML语言的界面设计，支持3D画布。
```

##### 1.3.2 界面的3种基类

```
QMainWindow:主窗口类，主窗口具有主菜单栏、工具栏和状态栏，类似于一般程序的主窗口
QWidget:所有具有可是界面的基类，选择QWidget创建的界面对各种界面组件都可以支持
QDialog:对话框类，可建立一个基于对话框的界面
```

#### 1.4 发布程序(以minGW为例)

```
注意：修改pro文件后，最好执行构建->重新构造项目，否则pro文件的更改将不会反应到程序上
发布程序的目的：就是让编译后生成的可执行文件(如exe文件)，能在其它计算机上运行
```

```
发布程序所需的几个动态库(debug模式下)
	libstdc++-6.dll:此文件不会提示缺失，缺少该文件或检测到多个该文件，会出现无法定位输入点的错误
	Qt5Cored.dll	115M
	Qt5Guid.dll		215M
	Qt5Widgetsd.dll	160M
```

```
手动发布程序及debug版本的缺点：
	debug版本发布的程序过于庞大(因为含有调试信息),解决此问题的方法是发布release版本(发布版本)的程序
	手动发布程序时容易漏掉需要的库文件(dll文件)
```

```
本地计算机运行exe文件的两种方法：
把exe文件复制到F:\app\Qt5.10.1\5.10.1\mingw53_32\bin(此目录为Qt安装时对应的mingw53_xx/bin,不唯一)目录下，直接运行即可
把以上路径设置为windows的环境变量,使用此方法后，不管生成的exe文件位于windows中的什么位置，都可直接双击运行
环境变量的设置方法：
	在“我的电脑上”，右击，选择“属性”，然后选择“高级系统设置”，找到“环境变量”,然后再"系统变量"栏目下找到"Path"变量，然后把以上变量添加到此变量中即可。
```

```
判断构造模式
	1.由构建时生成的文件夹名称可以判断出Qt Creator是以什么模式构建的项目，若名称最后是以debug则以debug模式构建，若名称最后是以release则以release模式构建。
	2.根据所生成的可执行文件的大小，可以判断出可执行文件最终是以什么模式生成的，使用debug模式生成的可执行文件会比release模式生成的可执行文件更大，因为debug模式会包含一些调试信息。
```

#### 1.5 moc简介

```
moc全称是meta-Object Compiler，即“元对象编译器”
因为Qt不是使用的标准C++语言，因此Qt在将源码交给标准C++编译器（如gcc）之前，需要先把拓展的语法先除掉，完成这一操作的就是moc
moc执行步骤：
	Qt程序编译之前，先试用moc分析c++源文件，若在头文件中包含了宏Q_OBJECT,则会生成另外一个包含了Q_OBJECT宏实现代码的C++源文件，这个新文件的名字是在原文件名之前加上moc_构成。这个新文件同样会进入到编译系统，最终被链接到二进制编译代码中去，因此我们在Qt构建后的文件夹中，见到moc_*.o和moc_*.cpp的文件，就是由moc生成的。注意：新文件不会替换掉旧文件，而是与原文件一起编译，另外，moc的编译是在预处理器之前。
```

#### 1.6 常用的Qt模块

```
注意：模块的名称都是以Qt开始的，类是以Q开始的
Qt Core:所有其它的Qt模块都依赖于这个模块，这是Qt的核心类库，提供了非GUI的核心功能
		主要有五大功能：即元对象系统、属性系统、对象模型、对象树、信号和槽
						另外还提供了一些额外的框架（比如状态机框架，动画框架等），还有线程、输入输出等功能
		相对于Qt4,Qt5中增加了对JSON的支持，并把XML移植到了该模块
		pro文件语法：QT += core,若使用qmake构造项目，则默认包含该模块
Qt GUI:这是图形用户界面(GUI)开发的最基础的模块，该模块提供了对图形用户界面的基本处理，包括窗口系统集成、事件处理、2D图形、基本图像、字体、文本、OpenGL、OpenGL ES集成等内容，相对于Qt4,Qt5把图形部件类(包括重要的QApplication)从该模块移植到了Qt Widgets模块，把对打印相关的移动到了Qt Print Support模块，同时把OpenGL相关类移动到了该模块，同时废除了以前的Qt OpenGL模块，pro文件语法：QT += gui,若使用qmake构建项目，则默认包含该模块
Qt Widgets:提供了C++用户界面部件	pro文件语法：QT += widgets
```

### 2.GUI应用程序设计基础

#### 2.1 UI文件设计与运行机制

```
项目文件组成（项目文件目录树）
	项目组织文件sample.pro：存储项目设置的文件
	主程序入口文件main.cpp：实现main()函数的程序文件
	窗体界面文件widget.cpp: 一个XML格式存储的窗体上的元件及其布局的文件。在C++里，任何窗体或界面组件都是用类封装的，一个类一般有一个头文件(.h文件)和一个源程序文件(.cpp文件)
```

##### 2.1.1模板代码Example

```c++
//表示项目中加入了core gui模块，core gui是Qt用于GUI设计的类库模块，如果创建的是控制台应用程序，就不需要添加core gui
//Qt类库以模块的形式组织各种功能的类，根据项目涉及的功能需求，在项目中添加适当的类库模块支持
//例如，如果项目中使用了涉及数据库操作的类就需要用到sql模块，在pro文件中需要增加如下一行:Qt += sql
QT += core gui	
//这是个条件执行语句，表示当Qt主版本大于4时，才加入widgets模块
greaterThan(Qt_MAJOR_VERSION,4): Qt += widget
//表示生成的目标可执行文件名称，即编译后生成的可执行文件
TARGET = sample
//表示项目使用的模板是app,是一般的应用程序
TEMPLATE = app
//项目中包含的源程序文件
SOURCES += main.cpp\
		widget.cpp
//项目中包含的头文件		
HEADERS += widget.h
//项目中包含的窗体文件
FORMS += widget.ui
```

##### 2.1.2 细讲界面文件.ui

```
UI设计器有以下一些功能区域
	1.组件面板：窗口左侧是界面设计组件面板，分为多个组，如Layouts、Buttons、Display Widgets等
	2.中间主要区域是待设计的窗体：如果要将某个组件放置到窗体上时，从组件面板上拖放一个组建到窗体上即可
	3.Signals和Slots编辑器与Action编辑器是位于待设计窗体下方的两个编辑器：
		Signals和Slots编辑器：用于可视化地进行信号与槽的关联
		Action编辑器:用于可视化设计Action
	4.布局和界面设计工具栏：窗口上方的一个工具栏，工具栏的按钮主要实现布局和界面设计
	5.对象浏览器(QObject Inspector)；窗口右上角是Object Inspector,用树状视图显示窗体上各组件之间的布局包含关系，视图有两列。显示每个组件的对象名称(ObjectName)和类名称
	6.属性编辑器(Property Editor):窗口右下方是属性编辑器，是界面设计时最常用到的编辑器。属性编辑区从上到下显示了当前组件类的继承关系，如在设计器中拖入一个QPushButton,那么将属性编辑器中属性最小化，不展开，即从上到下是QObject->QWidget->QAbstractButton->QPushButton
	objectName表示组件的对象名称，界面上每一个组件都需要一个唯一的对象名称，以便被引用。
```

提示：标准C++语言里并没有property关键字，property是Qt对标准C++的拓展，使得在Qt Designer里就可以可视化设置类的数据。

##### 2.1.3 细讲主函数文件main.cpp

```c
//main.cpp
main()函数是应用程序的入口。它的主要功能是创建应用程序，创建窗口，显示窗口，并运行应用程序，开始应用程序的消息循环和事件处理。
#include <Application>
#include "Widget"
int main(int argc, char *argv[]) //应用程序入口
{
	QApplication a(argc,argv); //创建应用程序
	
	Widget w;	//创建窗口
	w.show();	//显示窗口
	return a.exec(); //运行应用程序并开始应用程序的消息循环和事件处理
}
//QApplication:Qt的标准应用程序类，第6行代码定义了一个QApplication类的实例a,就是应用程序对象
//然后定义了一个Widget类的变量w,Widget是本实例设计的窗口的类名，定义此窗口后再用w.show()显示此窗口
//最后一行用a.exec() 启动应用程序的执行，开始应用程序的消息循环和事件处理
```

##### 2.1.4 窗体相关的文件（setupUi()详解）

```
setupUi():此函数用于生成界面，程序必须调用此函数，才能产生出界面，也就是说，虽然设计模式能拖放出界面的外观，但还是要编写代码来调用此函数以生成界面
```

```c++
//widget.h文件
#ifndef WIDGET_H		//防止头文件被重复引用	#ifndef #define #endif
#define WIDGET_H
#include <QWidget>

namespace Ui {		
    class Widget;
}

class Widget : public QWidget 
{
    Q_OBJECT	//信号和槽机制类必须有的宏
public:
    explicit Widget(QWidget *parent = 0);	//Widget的构造函数
    ~Widget();	//Widget的析构函数
private:
    Ui::Widget *ui;	//这个指针ui是指向可视化设计的界面，后面会看到访问界面上的组件，都需要通过这个指针ui
}
#endif

/*综上这是声明了一个名称为Ui的命名空间(namespace),包含一个类Widget,但是这个类并不是本文件里定义的类Widget
**而是ui_widget.h文件里定义的类，用于描述界面组件的，这个声明相当于一个外部类型声明
*/

//widget.cpp文件
#include "widget.h"
#include "ui_widget.h"	//自动加入的代码，这个就是Qt编译生成的与UI文件widget.ui对应的类定义文件
Widget::Widget (QWidget *parent) : QWidget(parent) , ui(new Ui::Widget) //执行父类QWidget的构造函数，创建一个Ui::Widget类的对象ui，这个ui就是Widget的private部分定义的指针变量ui
{
    ui->setupUi(this); //它是执行了Ui::Widget类的setupUi()函数，这个函数实现窗口的生成与各种属性的设置、信号与槽的关联
}
Widget::~Widget()
{
    delete ui; //简单地删除用new创建的指针ui
}
//NB666:ui->setupUi(this)  这个函数实现窗口的生成、各种属性的设置、信号和槽的关联
//详细说说:在ui_widget.h文件里有一个namespace名称为Ui,里面有一个类Widget是用于描述可视化设计的窗体，且与widget.h里定义的类同名。在Widget类里访问Ui::Widget类的成员变量或函数需要通过Widget类里的ui指针，如同构造函数里执行ui->setuiUi(this)函数那样

//widget.ui文件
widget.ui是窗体界面定义文件，是一个XML文件，定义了窗口上的所有组件的属性设置，布局，信号与槽函数关联等，用UI设计器可视化设计的界面都有Qt自动解析，并以XML文件形式保存下来。在设计界面时，只需在UI设计器里进行可视化设计即可，而不用管widget.ui文件是怎么生成的。

//ui_widget.h文件
ui_widget.h是对widget.ui文件编译后生成的一个文件，ui_widget.h会出现在编译后的目录下，或与widget.ui同目录(与项目的shadow build编译设置有关),文件ui_widget.h并不会出现在Qt Creator的项目文件目录树里，当然，可以手工将ui_widget.h添加到项目中。方法是在项目文件目录树上，右击项目名称节点，在调出的快捷菜单中选择“AddExisting Files ...”,找到并添加ui_widget.h文件即可。
即ui_widget.h是对widget.ui文件编译后自动生成的,widget.ui又是通过UI设计器可视化设计生成的，即 UI设计可视化设计 --->widget.ui ---> ui_widget.h,所以ui_widget.h也没有必要添加到项目里
```

```c
//ui_widget.h

#ifndef UI_WIDGET_H
#define UI_WIDGET_H
    
#include <QtCore/QVariant>
#include <QtWidgets/QAction>
#include <QtWidgets/QApplication>
#include <QtWidgets/QButtonGroup>
#include <QtWidgets/QHeaderView>
#include <QtWidgets/QLabel>
#include <QtWidgets/QPushButton>
#include <QtWidgets/QWidget>

Qt_BEGIN_NAMESPACE
class Ui_Widget //定义了一个类Ui_Widget，用于封装可视化设计的界面
{
public:
	QLabel *LabDemo;		    //自动生成了界面各个组件的类成员变量定义
    QPushButton *btnClose;		//自动生成了界面各个组件的类成员变量定义
    
    void setupUi(QWidget *widget)	//该函数用于创建各个界面组件、并设置其位置、大小、文字内容、字体等属性、设置信号槽关联
    {	//第一部分：根据可视化设计的界面内容，用C++代码创建界面上各组件，并设置其属性
        if (Widget->objectName().isEmpty())
//使用QStringLiteral宏可以在编译期把代码里的常量字符串 str 直接构造为 QString 对象，于是运行时就不再需要额外的构造开销了。 
            Widget->setObjectName(QStringLiteral("Widget"));
//设置窗口的大小，resize(w,h)	w:宽度	h：高度	也可以用setFixedSize(w,h)来代替resize(w,h)
//在窗口resize(w,h)时如果w或者h的值小于窗口内某个控件的w,h那么resize就在这个方向上无效此时Qt会自动生成一个合适的值
        Widget->resize(280,168);
        LabDemo = new QLabel(Widget);
        LabDemo->setObjectName(QStringLiteral("LabDemo")); 
//setGeometry(x,y,w,h); 从界面位置(x,y)开始的点，显示一个宽201，高51的界面
        LabDemo->setGeometry(QRect(50,20,201,51));
        QFont font;
        font.setPointSize(20);
        font.setBold(true);
        font.setWeight(75);
        LabDemo->setFont(font);
        btnClose = new QPushButton(Widget);
        btnClose->setObjectName(QStringLiteral("btnClose"));
        btnClose->setGeometry(QRect(150,120,75,23));
        //第二部分：用来设置界面各组件的文字内容属性，如标签的文字、按键的文件、窗体的标题等，将界面的文字设置的内容独立出来作为一个函数retranslateUi(),在设计多语言界面时会用到这个函数
        retranslateUi(Widget);	
        //第三部分：设置信号与槽的关联
        QObject::connect(btnClose,SIGNAL(clicked()),Widget,SLOT(close()));
        QMetaObject::connectSlotsByName(Widget); //设置槽函数的关联方式，用于将UI设计器自动生成的组件信号的槽函数与组建信号相关联
    } //所以，在Widget的构造函数里调用ui->setupUi(this)，就实现了窗体上组件的创建、属性设置、信号与槽的关联
    void retranslateUi(QWidget *widget)
    {
//QApplication::translate()界面中的字符串，参数1：类名 参数2：文本 参数3：消除歧义的注释，建议以后都用QObject::tr()
        Widget->setWindowTitle(QApplication::translate("Widget","My First Demo",Q_NULLPTR));
        Widget->setText(QApplication::translate("Widget","Hello,World",Q_NULLPTR));
        btnClose->setText(QApplication::translate("Widget","Close",Q_NULLPTR));
    }
};
//定义namespace Ui,并定义一个从Ui_Widget继承的类Widget
namespace Ui {
    class Widget : public Ui_Widget {};
}
Qt_END_NAMESPACE
#endif
    
//综上，ui_widget.h文件里实现界面功能的类是Ui_Widget。再定义一个类Widget从Ui_Widget继承而来，并定义在namespace Ui里，这样Ui::Widget与widget.h里的类Widget同名，但是用namespace区分开来。所以，界面的Ui::Widget类与文件widget.h里定义的Widget实际上是两个类，但是Qt的处理让用户感受不到Ui::Widget类的存在，只需要知道在Widget类里用ui指针可以访问可视化设计的界面组件就可以了
```

#### 2.2 可视化UI设计

##### 2.2.1 实例程序功能

```c++
详情参考代码samp2_2
对于界面组件的属性设置，需要注意以下几点：
1.objectName 是窗体上创建的组件的实例名称，界面上每一个组件需要有一个唯一的objectName,程序里访问界面组件时都是通过其objectName进行访问，自动生成的槽函数名称里也有objectName。所以，组件的objectName需要在设计程序之前设置好，设置好之后一般不要再改动。若设计程序之后再改动objectName,涉及的代码需要相应的改动。
2.窗体的objectName就是窗体的类名称，在UI设计器里不要修改窗体的objectName,窗体的实例名称需要在使用窗体的代码里去定义。
```

##### 2.2.2 界面组件布局

```c++
Qt的界面设置使用了布局（Layout）功能。
布局的定义：就是界面上组件的排列方式，使用布局可以是组件有规则地分布，并且随着窗体大小变化自动地调整大小和相对位置。
布局的意义；布局管理是GUI设计的必备技巧
```

###### 界面组件的层次关系

```c++
为了将界面上的各个组件的分布设计的更加美观，经常使用一些容器类，如QGroupBox、QTabWidget、QFrame等
```

###### 布局管理

```c++
/*	布局组件				功能
**Vertical Layout		垂直方向布局，组件主动在垂直方向上分布
**Horizontal Layout		水平方向布局，组件自动在水平方向上分布
**Grid Layout			网络状布局，网络布局大小改变时，每个网格的大小都改变
**Form Layout 			窗体布局，与网格状布局类似，但是只有最右侧的一列网格会改变大小
**Horizontal Spacer		一个用于水平分割的空格
**Vertical Spacer		一个用于垂直分隔的空格
*/
```

### 3.元对象系统、元对象、信号和槽

#### 3.1 元对象系统

```
Qt的元对象系统提供的功能：对象间通信的信号和槽机制、运行时类型信息和动态属性系统等
元对象系统是Qt对原有的C++进行一些拓展，主要是为实现信号和槽机制而引入的，信号和槽机制是Qt的核心特征。
要使用元对象系统的功能，需要满足以下三个条件：
	1.该类必须继承自QObject类
	2.必须在类声明的私有区域添加Q_OBJECT宏，该宏用于启动元对象特征，然后便可使用动态特性、信号和槽等功能了
	3.元对象编译器(moc)为每个QObject的子类，提供实现了元对象特征所必须的代码
元对象系统具体运行原则：
	1.因为元对象系统是为c++的拓展，因此使用传统的编译器是不能直接编译启用了元对象系统的Qt程序的，对此在编译Qt程序之前，需要把拓展的语法去掉，该功能就是moc需要做的事情了。
	2.moc全称是meta-Object Compiler(元对象编译器),它是一个工具(类似于qmake),该工具读取并分析C++源文件，若发现一个或多个包含了Q_OBJECT宏的类的声明，则会生成另外一个包含Q_OBJECT宏实现代码的C++源文件(该源文件通常名称为moc_*.cpp),这个新的源文件要么被#include 包含到类的源文件中，要么被编译间接到类的实现中(通常是使用此方法)。注意：新文件不会"替换"掉旧的文件，而是与原文件一起编译。
```

#### 3.2.元对象

```
QByteArray类简介：
	该类是一个用于处理字符串的类似于C++的string类型的类，在Qt中，对字符串的处理，经常使用的是QString类
	该类保证字符串以'\0'结尾，并使用隐式共享(copy-on-write)来减少内存用量和不必要的数据复制
	QByteArray适合用于存储纯二进制数据和内存资源比较短缺的情况下
```

```c++
示例：
#include <QByteArray>
#include <iostream>
using namespace std;

int main(int argc,char *argv[])
{
    QByteArray by("AAA"); //创建QByteArray的方式1
    const char *pc = "ABC";
    QByteArray by1(pc); //创建QByteArray的方式2
    const char *pc1 = by.data(); //返回指向该字符串的char *类型的指针
    cout << pc1 << endl; //输出AAA
    by1.append("DDD"); //在末尾追加字符串
    cout << by1.data() << endl;	//输出by1的字符串 ABCDDD
    cout << by1.size() << endl; //输出6,返回字符串的字符数(不含'\0')
    cout << by1[2] << endl; //使用下标访问单个字符，输出C
    cout << by1.at(1) << endl; //at()函数类似于下标算符，输出B
    return 0;
}
```

```
元对象系统与反射机制
reflection模式(反射模式或反射机制)：是指在运行时，能获取任意一个类对象的所有类型信息、属性、成员函数等信息的一种机制。
元对象系统与反射机制
	1、元对象系统提供的功能之一是为QObject派生类对象提供运行时的类型信息及数据成员的当前值等信息，也就是说，在运行阶段，程序可以获取QObject派生类对象所属类的名称、父类名称、该对象的成员函数、枚举类型、数据成员等信息，其实这就是反射机制。
	2、因为Qt的元对象系统必须从QObject继承，又从反射机制的主要作用可看到，Qt的元对象系统主要是为程序提供了QObject类对象及其派生类对象的信息，也就是说不是从QObject派生的类对象，则无法使用Qt的元对象系统来获取这些信息。
元对象：
	是指用于描述另一个对象结构的对象。使用编程语言具体实现时，其实就是一个类的对象，只不过这个对象专门用于描述另一个对象而已
	示例：
		class B 
		{
			xxx;
		};
		class A
		{
			B mb;
		};
		假设mb是用来描述类A创建的对象的，则mb就是元对象
```

### 4.事件√

```
继承关系:	QObject <--- QCoreApplication <--- QGuiApplication <---	QApplication	
一个程序只能有一个QCoreApplication及其子类的对象
QCoreApplicaton:主要用于提供无GUI的程序的事件循环
QGuiApplication:用于管理GUI程序的控制流和主要设置
QApplication:该类专门为QGuiApplication提供了基于QWidget的程序所需的一些功能，主要用于处理部件的初始化和最终化，主要职责：
	1.使用用户的桌面设置初始化应用程序
	2.执行事件处理，也就是说该类能从底层系统接收并分发事件
	3.解析常用命令行参数并设置其内部状态
	4.定义了应用程序的界面外观，可使用QApplication::setStyle()进行更改
	5.指定应用程序如何分配颜色
	6.使用QCoreApplicaton::translate()函数对字符串进行转换
	7.通过QCoreApplication::desktop()函数处理桌面，通过QCoreApplication::clipboard()函数处理剪切板
	8.管理应用程序的鼠标光标。比如使用QGuiApplication::setOverrideCuresor()函数设置光标等
什么是事件：是由程序内部或外部产生的事情或某种动作的通称。
```

#### 4.1五种处理事件的方法

```
√(常用)方法1：重写事件处理函数，比如QPaintEvent()、QMousePressEvent()函数，只能用来处理特定部件的特定事件
方法2：重写notify()函数，提供了完全控制，可以在事件过滤器得到事件之前就获得他们，但是需要继承自QApplicaton类，它只能一次处理		一个事件
方法3：重写event()函数
方法4：为QApplication对象安装事件过滤器，可以同时处理多个事件，但是要使用全局的事件过滤器
√(常用)方法5：在对象上安装事件过滤器，使用事件过滤器可以在一个界面类中同时处理不同子部件的不同事件
```

#### 4.2设置光标样式方法

```c++
QCursor cursor;								//创建光标对象
cursor.setShape(Qt::OpenHandCursor);		  //设置光标形状
setCursor(cursor); 							//使用当前光标
//一般在用户界面类的构造函数中就设置光标了
```

#### 4.3设置滚轮放大缩小字体

```c++
void wheelEvent(QWheelEvent *event)
{
	if (event->delta() > 0)
        ui->textEdit->zoomIn();
    else
        ui->textEdit->zoomOut();
}
```

#### 4.4鼠标双击放大屏幕

```c++
void mouseDoubleClickEvent(QMouseEvent *event)
{
	if (event->button() == Qt::LeftButton())
	{
		if (windowState() != Qt::WindowFullScreen)
			setWindowState(Qt::WindowFullScreen);
		else
			setWindowState(Qt::WindowNoState);
	}	
}
```

#### 4.5globalPos()和pos()鼠标指针位置

```
globalPos():获取鼠标指针的位置，这个位置是指针在桌面上的位置，因为窗口的位置就是指它在桌面上的位置
pos():获取鼠标指针在窗口中的位置
```

#### 4.6鼠标移动事件

```c++
void mouseMoveEvent(QMouseEvent *event)
{
	if (event->buttons() & Qt::LeftButton) //因为鼠标移动时会检测所有按下的键，而这时使用event->button()无法检测哪个键被按下，只能使用buttons()函数，所以这里使用event->buttons()和Qt::LeftButtons按位与的方法来判断是否鼠标左键被按下
	{
		QPoint temp;
		temp = event->globalPos()-offset; //偏移差值offset = globalPos() - pos()
		move(temp); //使用鼠标当前位置减去差值，就得到了窗口应该移动到的位置
	}
}
```

#### 4.7setMouseTracking(true)设置鼠标移动默认跟踪

```c++
默认是当按下鼠标按键时移动鼠标，鼠标移动事件才会产生
如果想不按鼠标按键，也可以获取鼠标移动事件，那么就要在构造函数中添加下面一行代码
setMouseTracking(true);	//设置鼠标跟踪，这样便会开启窗口部件的鼠标跟踪功能
```

#### 4.8setWindowState()之windowState的可选枚举

```c++
enum WindowState
{
	WindowNoState,		//窗口无状态
	WindowMinimized,	//窗口最小化
	WindowMaximized,	//窗口最大化
	WindowFullScreen,	//窗口满屏
	WindowActive		//窗口动作
};
```

#### 4.9setWindowFlag()之WindowType

```c++
    enum WindowType {
        Widget = 0x00000000,
        Window = 0x00000001,
        Dialog = 0x00000002 | Window,
        Sheet = 0x00000004 | Window,
        Drawer = Sheet | Dialog,
        Popup = 0x00000008 | Window,
        Tool = Popup | Dialog,
        ToolTip = Popup | Sheet,
        SplashScreen = ToolTip | Dialog,
        Desktop = 0x00000010 | Window,
        SubWindow = 0x00000012,
        ForeignWindow = 0x00000020 | Window,
        CoverWindow = 0x00000040 | Window,

        WindowType_Mask = 0x000000ff,
        MSWindowsFixedSizeDialogHint = 0x00000100,
        MSWindowsOwnDC = 0x00000200,
        BypassWindowManagerHint = 0x00000400,
        X11BypassWindowManagerHint = BypassWindowManagerHint,
        FramelessWindowHint = 0x00000800,
        WindowTitleHint = 0x00001000,
        WindowSystemMenuHint = 0x00002000,
        WindowMinimizeButtonHint = 0x00004000,
        WindowMaximizeButtonHint = 0x00008000,
        WindowMinMaxButtonsHint = WindowMinimizeButtonHint | WindowMaximizeButtonHint,
        WindowContextHelpButtonHint = 0x00010000,
        WindowShadeButtonHint = 0x00020000,
        WindowStaysOnTopHint = 0x00040000,
        WindowTransparentForInput = 0x00080000,
        WindowOverridesSystemGestures = 0x00100000,
        WindowDoesNotAcceptFocus = 0x00200000,
        MaximizeUsingFullscreenGeometryHint = 0x00400000,

        CustomizeWindowHint = 0x02000000,
        WindowStaysOnBottomHint = 0x04000000,
        WindowCloseButtonHint = 0x08000000,
        MacWindowToolBarButtonHint = 0x10000000,
        BypassGraphicsProxyWidget = 0x20000000,
        NoDropShadowWindowHint = 0x40000000,
        WindowFullscreenButtonHint = 0x80000000
    };
```



#### 4.10修饰键需要用QKeyEvent的modifiers()函数来获取（Ctrl、shift等）

```c++
    enum KeyboardModifier 
    {
        NoModifier           = 0x00000000,
        ShiftModifier        = 0x02000000,
        ControlModifier      = 0x04000000,
        AltModifier          = 0x08000000,	
        MetaModifier         = 0x10000000,	//对应键盘的win键，即左下角Ctrl和Alt中间的键
        KeypadModifier       = 0x20000000,	//对应的键盘右边的数字区0-9，+-*/等
        GroupSwitchModifier  = 0x40000000,	//虚拟句柄键
        // Do not extend the mask to include 0x01000000
        KeyboardModifierMask = 0xfe000000
    };
```

#### 4.11回车键对应的枚举成员Qt::Key_Return,判断某个键是否重复按下的函数QEvent::isAutoRepeat()

#### 4.12 定时器事件

```c++
//1.QTimerEvent类用来描述一个定时器事件
//2.对于一个QObject子类，只需要用 int QObject::startTimer(int 	interval)就可以开启一个定时器，这个函数需要输入一个以毫秒为单位的整数作为参数来表明设定的时间，函数返回一个整型编号来代表这个定时器，当定时器溢出时可以在timerEvent()函数中进行需要的操作
//3.其实编程中更多的是使用QTimer类来实现一个定时器，它提供了更高层次的编程接口，比如可以使用信号和槽，还可以设置只运行一次的定时器，所以在以后使用定时器中，一般是使用QTimer类
//4.开启一个只运行一次的定时器singleShot()
	//这里将时间设置为10S,溢出时便调用窗口部件的close()函数来关闭窗口
	QTimer::singleShot(10000,this,&Widget::close);	//程序运行10000ms(10s)后当前的Widget窗口关闭
```

```c++
//方法1：startTimer() 自动触发到 timerEvent(QTimerEvent *event)	！！！
int id1,id2,id3;
id1 = startTimer(1000);	//用startTimer()直接开启事件，参数单位是ms
id2 = startTimer(1500);
id3 = startTimer(2000);

startTimer()这个函数待时间到达会自动触发void timerEvent(QTimerEvent *event)函数
//获取定时器的方法：
void timerEvent(QTimerEvent *event)
{
    if (event->timerId() == id1)
        qDebug() << "timer1" << endl;
    else if (event->timerId() == id2)
        qDebug() << "timer2" << endl;
    else 
        qDebug() << "timer3" << endl;
}
```

```c++
//方法2：QTimer::start()自动触发QTimer::timeout()
QTimer *timer = new QTimer(this);
timer->start(1000); //设置溢出时间为1s,并启动定时器。1s后自动触发QTimer::timeout()
connect(timer,&QTimer::timeout,this,&Widget::timeUpdate); //Widget::timeUpdate是自定义的槽函数，可任意
```

##### QTime::second()获取秒的值

```c++
QTime time = QTime::currentTime();
QString text = time.toString("hh:mm");
if ((time.second() % 2) == 0)
	text[2] = " "; 			//每隔1s就将“：”显示为空格
ui->lcdNumber->display(text);	
```



#### 4.13 随机数qrand()和qsrand()

```c++
//在使用qrand()产生随机数之前，一般要使用qsrand()函数为其设置初值，如果不设置初值，那么每次运行程序qrand()都会产生相同的一组随机数，为了每次运行时都可以产生不同的随机数，那么就要使用qsrand()设置一个不同的初值。这里使用了QTime类的secsTo()函数，它表示两个时间点之间所包含的秒数，比如代码中就是指从零点整到当前时间所经过的秒数
qsrand(QTime(0,0,0).secsTo(QTime::currentTime()));	//QTime(小时，分钟，秒)	即0时0分0秒
int rand = qrand() % 300;	//产生300以内的正整数	0~299
```

#### 4.14 事件过滤器

```c++
//Qt中提供了事件过滤器来实现在一个部件中监控其它多个部件的事件
//事件过滤器不是一个类，只是由两个函数组成的一种操作，用来完成一个部件对其它部件的事件的监视
//两个函数installEventFilter()和eventFilter(),都是Object中的函数
//要对一个部件使用事件过滤器，那么就要先使用其的installEventFilter()函数为其安装事件过滤器，这个函数的参数表明了监视对象

ui->textEdit->installEventFilter(this); 
ui->spinBox->installEventFilter(this);
//其参数this表明要在本部件(即Widget)中监视textEdit和spinBox事件，这样就需要重新实现Widget类中的eventFilter()函数，在其中截获并处理两个子部件的事件。

bool eventFilter(QObject *obj, QEvent *event)
{
    if (obj == 组件1名称)
    {
        if (event->type() == QEvent::type的枚举成员)	//比如QEvent::Wheel
        {
            xxx;
        }
        else
        {
            xxxxxx;
        }
    }
    else if (obj == 组件2名称)
    {
        if (event->type() == QEvent::type的枚举成员)	//比如QEvent::KeyPress,QEvent::MouseButtonPress
        {
            xxx;
        }
        else
        {
            xxxxxx;
        }
    }
    return QWidget::eventFilter(obj,event);
}

//示例：
bool eventFilter(QObject *obj, QEvent *event)
{
    if (obj == ui->textEdit)
    {
        if (event->type == QEvent::Wheel)
        {
            QWheelEvent *wheelEvent = static_cast<QWheelEvent*>(event);
            if (wheelEvent->delta() > 0)
               	ui->textEdit->zoomIn();
            else
                ui->textEdit->zoomOut();
            return true;				//该事件已被处理
        }
        else
        {
            return false;	//如果是其它事件，可以进行进一步处理
        }
    }
    else if (obj == ui->spinBox)
    {
        if (event->type == QEvent::KeyPress)
        {
            QKeyEvent *keyEvent = static_cast<QKeyEvent*>(event);
            if (keyEvent->key() == Qt::QKey_Space)
            {
                ui->spinBox->setValue(0);
                return true;
            }
            else
                return false;
        }
        else 
            return false;
    }
    else
        return QWidget::eventFilter(obj,event);
}
//综上示例，概述
//在这个事件过滤器中，先判断部件的类型，然后再判断事件的类型，如果是需要的事件，那么就将其进行强制类型转换，然后进行相应的处理。特别说明：如果要对一个特定的事件进行处理，而且不希望它在后面的传递过程中再被处理，那么就返回true，否则返回false;这个函数实现了在textEdit部件中使用滚轮进行内容的放大或缩小，在spinBox部件中使用空格来使数值设置为0。

Qt中提供了发送一个事件的功能，它由QCoreApplication类的
    bool QCoreApplication::sendEvent(QObject *receiver, QEvent *event)函数，或者
    void QCoreApplication::postEvent(QObject *receiver, QEvent *event, int priority = Qt::NormalEventPriority)
sendEvent()会立即处理给定的事件，sendEvent（）中的QEvent对象参数在事件发送完成后无法自动删除，所以需要在栈上创建QEvent对象
postEvent()会将事件放到等待调度队列中，当下一次Qt的主事件循环运行时才会处理它。而postEvent()中的QEvent对象参数必须在堆上进行创建(例如使用new),当事件被发送后事件队列会自动删除它。
```

##### qApp

```c++
QKeyEvent myEvent(QEvent::KeyPress, Qt::Key_Up, Qt::NoModifier);
qApp->sendEvent(ui->spinBox,&myEvent);	//发送键盘事件到spinBox部件
qApp是QCoreApplication的全局指针，每一个应用程序只能使用一个QApplication对象，等价于使用QApplication::sendEvent()
```



##### 强制类型转换static_cast<type>(parm)

```c++
static_cast<tpye>(parm)	//将parm的数据类型强制转换成type类型的
//示例
    int n = static_cast<int>(3.1415926); //经过转换后，n = 3
```



## 二、技术专栏

#### 1.1 "你好Qt"的多重B格😎

B1:调用第三方类

```c++
    QApplication a(argc, argv);
    HelloDialog w;
    w.show();
```

B2:开门见山之调系统对象QLabel

```c++
    QApplication a(argc, argv);
    QDialog w;
    w.resize(400, 300);
    QLabel label(&w);
    label.move(120, 120);
    label.setText(QObject::tr("Hello World! 你好Qt！"));
    w.show();
    return a.exec();
```

B3:开门见山之调自己绘制的Ui

```c++
    QApplication a(argc, argv);
    QDialog w;
    Ui::HelloDialog ui;
    ui.setupUi(&w);
    w.show();
    return a.exec();
```

#### 1.2 RC_ICONS程序图标使用

````c++
说明
   	1.本技术是实现QtCreator修改生成的程序的图标样子，新的样子为myico.ico
    2.修改位置在Qt程序代码的pro文件中添加
    3.myico.ico可以指定绝对路径或相对路径，如果不选择路径，默认路径应该为xxx.pro所在的路径，非exe路径！！！
    
代码
xxx.pro
    RC_ICONS = myico.ico
````

#### 1.3 只要一个main，就有一个exe

##### 1.3.1隐藏窗口Qt::FramelessWindowHint/resize

```c++
   int main(int argc,char argv[])
   {
       QApplication a(argc, argv);

        // 新建QWidget类对象，默认parent参数是0，所以它是个窗口 
        QWidget *widget = new QWidget(0, Qt::Dialog | Qt::FramelessWindowHint);
        // 设置窗口标题
        widget->setWindowTitle(QObject::tr("我是widget"));
        // 新建QLabel对象，默认parent参数是0，所以它是个窗口
        QLabel *label = new QLabel(0, Qt::SplashScreen | Qt::WindowStaysOnTopHint);
        label->setWindowTitle(QObject::tr("我是label"));
        // 设置要显示的信息
        label->setText(QObject::tr("label:我是个窗口"));
        // 改变部件大小，以便能显示出完整的内容
        label->resize(180, 20);
        // label2指定了父窗口为widget，所以不是窗口
        QLabel *label2 = new QLabel(widget);
        label2->setText(QObject::tr("label2:我不是独立窗口，只是widget的子部件"));
        label2->resize(250, 20);
        // 在屏幕上显示出来
        label->show();
        widget->show();

       //这个操作值得学习
        int ret = a.exec();
        delete label;
        delete widget;
        return ret;
    }
```

##### 1.3.2geometry()和frameGeometry()

![Qt_geometry](C:\Users\Gaopeng\Pictures\Saved Pictures\Qt_geometry.png)

```c++
说明：
x()：左上角的坐标（屏幕左上角是远点（0,0））
y()：左上角的坐标（屏幕左上角是远点（0,0））
width()：客户区的宽度
height()：客户区的高度
geometry.x()：不包括标题栏、边框的客户区
geometry.y()：不包括标题栏、边框的客户区
geometry.width()：客户区的宽度
geometry.height()：客户区的高度
frameGeometry.x()：左上角的坐标
frameGeometry.y()：左上角的坐标
frameGeometry.width()：窗口真正的宽度（包括边框和标题栏）
frameGeometry.height()：窗口真正的高度（包括边框和标题栏）

代码：
int main(int argc, char *argv[])
{
    QApplication a(argc, argv);

    QWidget widget;
    widget.resize(400, 300);       // 设置窗口大小
    widget.move(200, 100);         // 设置窗口位置
    widget.show();
    int x = widget.x();
    qDebug("x: %d", x);            // 输出x的值
    int y = widget.y();
    qDebug("y: %d", y);
    QRect geometry = widget.geometry();
    QRect frame = widget.frameGeometry();
    qDebug() << "geometry: " << geometry << "frame: " << frame;

    return a.exec();
}

result:
x: 200
y: 100
geometry:  QRect(201,138 400x300) frame:  QRect(200,100 402x339)
```

#### 1.4QDialog的花花世界

```c++
MyWidget::MyWidget(QWidget *parent) :
    QWidget(parent),
    ui(new Ui::MyWidget)
{
    ui->setupUi(this);
    QDialog *dialog = new QDialog(this);
    dialog->setModal(true); //设置为模态对话框
    dialog->show();
}
```

##### 1.4.1调用控件的手撕信号槽法和右键直连法

```c++
1.手撕信号槽法   
    connect(ui->showChildButton, &QPushButton::clicked,this, &MyWidget::showChildDialog);
    void MyWidget::showChildDialog()
    {
        QDialog *dialog = new QDialog(this);
        dialog->show();
    }

2.designed ui右键直连法
    void MyWidget::on_showChildButton_clicked()
    {
        QDialog *dialog = new QDialog(this);
        dialog->show();
    }
```

##### 1.4.2 ✔铁子，这才叫做对话框🐱‍🚀（3-7）

```c++
MyWidget::MyWidget(QWidget *parent) :
    QWidget(parent),
    ui(new Ui::MyWidget)
{
    ui->setupUi(this);
    errordlg = new QErrorMessage(this);
}

MyWidget::~MyWidget()
{
    delete ui;
}

// 颜色对话框
void MyWidget::on_pushButton_clicked()
{
    //这里使用了QColorDialog的静态函数getColor()来获取颜色，文件头写#include <QColorDialog>
    //它的3个参数的作用分别是：设置初始颜色，指定父窗口，设置对话框标题
    //getColor()返回一个QColor类型的数据，这个返回的数据为QColor(arg1,arg2,arg3,arg4)
    //arg1代表透明度(alpha)、红色(red)、绿色(green)、蓝色(blue)它们的数值都是从0.0~1.0，有效数字为6位
    //对于alpha来说，1.0表示完全不透明，这时默认值，而0.0表示完全透明，对于三基色红绿蓝的数值，还可以使用0~255来表示，
    //颜色对话框就是使用这种方法，其中0表示颜色最浅，255表示颜色最深
    //在0~255与0.0~1.0之间可以通过简单的数学运算来对应，其中0对应0.0,255对应1.0
    //在颜色对话框中还可以添加对alpha的设置，就是在getColor()函数中再使用最后一个参数，QColorDialog::ShowAlphaChannel
    
    //方法1：直接显示alpha设置
    //QColor color = QColorDialog::getColor(Qt::red, this, tr("颜色对话框"),QColorDialog::ShowAlphaChannel);

    //方法2：灵活显示alpha设置 30-32行就可以了
    QColorDialog dialog(Qt::red, this);                // 创建对象，参数1和2，设置初始颜色，指定父对象
    dialog.setOption(QColorDialog::ShowAlphaChannel); // 参数4：显示alpha选项
    dialog.exec();                                    // 以模态方式运行对话框
    QColor color = dialog.currentColor();             // 获取当前颜色
    qDebug() << "color: " << color;
    
    //方法1和方法2是等效的
}

// 文件对话框
void MyWidget::on_pushButton_2_clicked()
{
    //文件对话框QFileDialog类提供了一个允许用户选择文件或文件夹的对话框，文件头写#include <QFileDialog>
    //这里使用了QFileDialog::getOpenFileName()来获取选择的文件名，这个函数会以模态方式运行一个文件对话框
    //打开后，选择一个文件，单击"打开"按钮后，这个函数便可以返回选择的文件的文件名 返回类型是QString
    //它的四个参数作用分别是：指定父窗口，设置对话框标题，指定默认打开的目录路径，设置文件类型过滤器
    //如果不指定文件过滤器，则默认选择所有类型的文件
    //这里指定了只选择png和jpg两种格式的图片文件（注意，代码中*png和*jpg之间需要一个空格），那么在打开的文件对话框中只能显示目录下这两种格式的文件
    //还可以设置多个不同类型的过滤器，不同类别间使用两个分号";;"隔开
    //getOpenFileName()只能选择单个文件，如果同时选择多个文件，则可以使用getOpenFileNames()函数，返回值是QStringList
    //除了getOpenFileName(),QFileDialog还提供getSaveFileName()函数来实现保存文件对话框和文件另存为对话框
    
    //选择单个文件
    //    QString fileName = QFileDialog::getOpenFileName(this, tr("文件对话框"),
    //                             "D:", tr("图片文件(*png *jpg);;文本文件(*txt)"));
    //    qDebug() << "fileName:" << fileName;

    //选择多个文件
    QStringList fileNames = QFileDialog::getOpenFileNames(this, tr("文件对话框"),
                                                          "D:", tr("图片文件(*png *jpg)"));
    qDebug()<< "fileNames:" << fileNames;
}

// 字体对话框
void MyWidget::on_pushButton_3_clicked()
{
    //字体对话框提供了一个可以选择字体的对话框部件，先添加#include <QFontDialog>
    // ok用于标记是否按下了“OK”按钮
    bool ok; //用来存放按下的按钮状态
    QFont font = QFontDialog::getFont(&ok, this);
    // 如果按下“OK”按钮，那么让“字体对话框”按钮使用新字体
    // 如果按下“Cancel”按钮，那么输出信息
    if (ok) ui->pushButton_3->setFont(font);
    else qDebug() << tr("没有选择字体！");
}

// 输入对话框
void MyWidget::on_pushButton_4_clicked()
{
    bool ok;
    // 获取字符串
    //参数1,2,3,4分别代表指定父窗口，设置窗口标题，设置对话框中的标签显示文本，设置输入字符串的显示模式（例如密码可以显示成小黑点，这里选择了显示用户输入的实际内容）、设置输入框中的默认字符串，设置获取按下按钮信息的bool变量
    QString string = QInputDialog::getText(this, tr("输入字符串对话框"),
                                           tr("请输入用户名："), QLineEdit::Normal,tr("admin"), &ok);
    if(ok) qDebug() << "string:" << string;
    
    // 获取整数 父对象，dlg标题，dlg标签，默认值，min,max,step,return
    int value1 = QInputDialog::getInt(this, tr("输入整数对话框"),
                                      tr("请输入-1000到1000之间的数值"), 100, -1000, 1000, 10, &ok);
    if(ok) qDebug() << "value1:" << value1;
    
    // 获取浮点数 父对象，dlg标题，dlg标签，默认值，min,max,step,return
    double value2 = QInputDialog::getDouble(this, tr("输入浮点数对话框"),
                                            tr("请输入-1000到1000之间的数值"), 0.00, -1000, 1000, 2, &ok);
    if(ok) qDebug() << "value2:" << value2;
    
    
    QStringList items; 
    items << tr("条目1") << tr("条目2"); //需要提供一些条目
    // 获取条目 父对象，dlg标题，dlg标签，可输入的条目，默认显示列表中的第0个条目，条目是否可以被更改，true就是可以被更改，
    QString item = QInputDialog::getItem(this, tr("输入条目对话框"),
                                         tr("请选择或输入一个条目"), items, 0, true, &ok);
    if(ok) qDebug() << "item:" << item;
}

/*消息对话框，各类之间的区别对比
*问题对话框QMessageBox::question:
	5个参数：父对象，dlg标题，dlg显示内容，左下显示的按钮QMessageBox::Yes，右下显示的按钮QMessageBox::No
	返回值:int ret == QMessageBox::Yes | QMessageBox::No
	应用:可通过返回值不同执行不同的操作

*提示对话框QMessageBox::information:
	4个参数:父对象，dlg标题，dlg显示内容，下面显示的按钮(提示专属)QMessageBox::OK
	返回值:int ret = QMessageBox::Ok
	应用:用于起提示作用时使用

*警告对话框QMessageBox::warning:
	4个参数:父对象，dlg标题，dlg显示内容，下面显示的按钮（警告专属）QMessageBox::abort
	返回值:int ret = QMessageBox::Abort
	应用:起警告作用
	
*错误对话框QMessageBox::critical:
	4个参数：父对象，dlg标题，dlg显示内容，下面显示的按钮（错误专属）QMessageBox::YesAll
	返回值:int ret = QMessageBox::YesAll
	应用：用于报错时使用

*关于对话框QMessageBox::about:
	3个参数:父对象，dlg标题，dlg显示的内容
	返回值：无
*/

// 消息对话框
void MyWidget::on_pushButton_5_clicked()
{
    // 问题对话框 父窗口，dlg标题，dlg显示的信息，dlg拥有的按钮
    int ret1 = QMessageBox::question(this, tr("问题对话框"),
                                     tr("你了解Qt吗？"), QMessageBox::Yes, QMessageBox::No);
    if(ret1 == QMessageBox::Yes) qDebug() << tr("问题！");
    
    // 提示对话框
    int ret2 = QMessageBox::information(this, tr("提示对话框"),
                                        tr("这是Qt书籍！"), QMessageBox::Ok);
    if(ret2 == QMessageBox::Ok) qDebug() << tr("提示！");
    
    // 警告对话框
    int ret3 = QMessageBox::warning(this, tr("警告对话框"),
                                    tr("不能提前结束！"), QMessageBox::Abort);
    if(ret3 == QMessageBox::Abort) qDebug() << tr("警告！");
    // 错误对话框
    int ret4 = QMessageBox::critical(this, tr("严重错误对话框"),
                                     tr("发现一个严重错误！现在要关闭所有文件！"), QMessageBox::YesAll);
    if(ret4 == QMessageBox::YesAll) qDebug() << tr("错误");
    // 关于对话框
    QMessageBox::about(this, tr("关于对话框"),
                       tr("yafeilinux致力于Qt及Qt Creator的普及工作！"));
}

// 进度对话框	设置对话框的标签内容，取消按钮的显示文本，最小值，最大值，父窗口
void MyWidget::on_pushButton_6_clicked()
{
    QProgressDialog dialog(tr("文件复制进度"), tr("取消"), 0, 50000, this);
    dialog.setWindowTitle(tr("进度对话框"));     // 设置窗口标题
    dialog.setWindowModality(Qt::WindowModal);  // 将对话框设置为模态
    dialog.show();
    for(int i=0; i<50000; i++) {                // 演示复制进度
        dialog.setValue(i);                     // 设置进度条的当前值
        QCoreApplication::processEvents();      // 避免界面冻结（为了避免长时间操作而使用户界面冻结）
        if(dialog.wasCanceled()) break;         // 按下取消按钮则中断（判断用户是否按下了取消按钮）
    }
    dialog.setValue(50000);    // 这样才能显示100%，因为for循环中少加了一个数
    qDebug() << tr("复制结束！");
}

// 错误信息对话框
void MyWidget::on_pushButton_7_clicked()
{
    QErrorMessage *errordlg = new QErrorMessage(this);
    errordlg->setWindowTitle(tr("错误信息对话框"));
    errordlg->showMessage(tr("这里是出错信息！"));
}

// 向导对话框
//向导对话框QWizard类提供了一个设计向导界面的框架，安装软件时的向导和创建项目时的向导
//1.需要包括QWizard类，#include <QWizard>
//2.创建QWizardPage *的函数

QWizardPage * MyWidget::createPage1()  // 向导页面1
{
    QWizardPage *page = new QWizardPage;
    page->setTitle(tr("介绍"));
    return page;
}
QWizardPage * MyWidget::createPage2()  // 向导页面2
{
    QWizardPage *page = new QWizardPage;
    page->setTitle(tr("用户选择信息"));
    return page;
}
QWizardPage * MyWidget::createPage3()  // 向导页面3
{
    QWizardPage *page = new QWizardPage;
    page->setTitle(tr("结束"));
    return page;
}

QWizardPage* addPage1();
//实现：
QWizaedPage* MyWidget::addPage1()
{
    QWizardPage *page = new QWizardPage;
    page->setTitle(tr("介绍"));
    return page;
}
QWizardPage* addPage2()
{
    QWizardPage *page = new QWizardPage;
    page->setTitle(tr);
    return page;
}
QWizardPage* addPage3()
{
    QWizardPage *page = new QWizardPage;
    page->setTitle(page);
    returm
}

void MyWidget::on_pushButton_8_clicked()
{
    QWizard wizard(this);
    wizard.setWindowTitle(tr("向导对话框"));
    wizard.addPage(createPage1());     // 添加向导页面
    wizard.addPage(createPage2());
    wizard.addPage(createPage3());
    wizard.exec();
}
```

#### 1.5 文件、目录和输入输出

##### 1.5.1.输入/输出设备QIODevice

```c++
/*QIODevice的打开方式
* QIODevice::NotOpen						设备没有打开
* QIODevice::ReadOnly						设备以只读方式打开，这时无法写入
* QIODevice::WriteOnly						设备以只写方式打开，这时无法读取
* QIODevice::ReadWrite						设备以读写方式打开
* QIODevice::Append						    设备以附加模式打开，所有数据将写入到文件的末尾
* QIODevice::Truncate						如果可能，设备在打开前会被截断，设备先前所有的内容都将丢失
* QIODevice::Text						    当读取时，行结尾终止符会被转换为"\n"
										  当写入时，行结尾终止符会被转换为本地编码，例如在Win32上是"\r\n"
* QIODevice::Unbuffered						绕过设备所有的缓冲区
*/

/* QIODevice设备分类
* 随机存储设备
	1.支持使用seek()函数来定义到任意位置
	2.支持使用pos()函数来获取文件中的当前位置
	3.如QFile和QBuffer等
* 顺序存储设备
	1.不支持定义到任意的位置，设备必须一次性读取
	2.不支持使用pos()和size()等函数
	3.如QTcpSocket和QProcess等
* 判断设备类型的方法
	1.使用isSequential()函数来判断设备的类型
*/

/*要子类化QIODevice，则只需要重新实现readData()和writeData()这两个函数
* QIODevice的一些子类，比如QFile和QTcpSocket，都使用了内存缓冲区进行了数据的中间存储，这样减少了设备的访问次数
* 使得getChar()和putChar()等函数可以快速执行，而且可以在内存缓冲区上操作，而不用直接在设备上进行操作，但是一些
* 特定的IO操作缓冲区无法很好地工作，这时就可以调用open()函数打开设备时使用QIODevice::Unbuffered模式来绕过所有的缓冲区
*/
```



##### 1.5.2 文件操作QFile和FILE

```c++
QFile
    setFileName()		设置文件名
    exists()			检查文件是否存在
    remove()			删除一个文件
    open()				打开文件
    close()				关闭文件
    flush()				刷新
    
QDataStream				文件的数据读写
QTextStream				文件的数据读写
    
继承QIODevice的函数
    	read()
    	readLine()
    	readAll()
    	write()
    
一次只操作一个字符的函数
    	getChar()
    	putChar()
    	ungetChar()

    size():获取文件大小
    seek():定位文件的任意位置
    pos():获取当前位置
    atEnd():是否达到了文件的末尾
	
//example
    
    //一、写
    QFile file("example.txt");
	if(!file.open(QIODevice::WriteOnly | QIODevice::Text))
        qDebug() << "写入异常消息:" << file.errorString();
	file.write("Hello,Qt!\nyafeiLinux");
	file.close();

	//二、查
	QFileInfo info(file);
	qDebug() << "当前文件的绝对路径:" << info.absolutionFilePath() << endl;
	qDebug() << "当前文件的名称:" << info.fileName() << endl;
	qDebug() << "当前文件的基本名称:" << info.baseName() << endl;
	qDebug() << "当前文件的后缀名称:" << info.suffix() << endl;
	qDebug() << "当前文件的创建时间" << info.created() << endl;
	qDebug() << "当前文件的大小:" << info.size() << endl;

	//三、读
	if(!file.open(QIODevice::ReadOnly | QIODevice::Text))
        qDebug() << "读取异常消息:" << file.errorString();
	qDebug() << "文件的所有内容:" << file.readAll();
	qDebug() << "当前光标所在位置:" << file.pos();
	QByteArray array;
	file.seek(0); //将光标置于第一个字符之前
	array = file.read(5); //读取前5个字符
	file.seek(15);
	array = file.read(5); //读取第16到20个字符
	file.close();

//example2
	QString strPath = QCoreApplication::applicationDirPath() + "/test.txt";
	FILE *fp = NULL;
	fp = fopen(strPath.toLocal8Bit().constData(),"rb");
	if (NULL == fp)
    {
		qDebug() << "文件打开失败" << endl;
        return;
    }
	
```



##### 1.5.3 目录操作QDir

```c++
//1.QDir：用来访问目录结构及其内容，可以操作路径名，访问路径和文件相关信息，操作底层的文件系统，还可以访问Qt的资源系统
//2.QDir可以使用相对路径或者绝对路径来指向一个文件
	QDir dir("/home/user/Documents"); 		//绝对路径示例1
	QDir dir("C:/Doucuments and Settings");	//绝对路径示例2	在windows中，会将其转换为C：\Documents and Settings
	QDir dir("images/lanscaped.png"); //相对路径示例
//3.判断QDir是否使用了相对路径和绝对路径
	isRelative(); //判断是否使用了相对路径
	isAbsolute(); //判断是否使用了绝对路径
//4.路径转换
	makeAbsolute(); //将一个相对路径转换成绝对路径
//常用函数
	path() //获取一个目录的路径
    setPath() //设置新的路径
    absloutePath() //获取绝对路径
    dirName() //获取目录名
    cd() / cdUp() //改变目录的路径		cd相当于linux 中的'.'（当前目录）		cdUp相当于linux的'..'上级目录（父目录）
    mkdir() //创建目录
    rename() //重命名目录
    redir() //删除目录
    exists() //测试指定的目录是否存在
    isReadable() //测试目录的属性
    isRoot() //测试目录的属性
    refresh() //重新读取目录的数据
    count() //返回目录的条目数目
    entryList() //返回所有条目的名称列表
    entryInfoList() //获取一个QFileInfo对象的列表
    filePath() //获取一个目录中的文件和目录的路径，返回指定文件或目录与当前QDir对象所在路径的相对路径
    absoluteFilePath() //获取一个目录中的文件和目录的路径，返回指定文件或目录与当前QDir对象所在路径的绝对路径
    remove() //移除文件
    rmdir() //移除目录（只能移除目录）
    QCoreApplication::applicationDirPath()	//包含应用程序可执行文件的目录
    drives() //返回系统的根目录
//名称过滤器（字符串列表）：可以应用一个名称过滤器来使用通配符指定一个模式进行文件名的匹配
	QStringList filters;
	filters << "*.cpp" << "*.cxx" << "*.cc";
	dir.setNameFilters(filters);

//文件系统监视器QFileSystemWatcher：监控文件和目录的修改，通过监视一个指定路径的列表来监控文件系统中文件和目录的改变
//调用addPath()来监视一个指定的文件或者目录，多个路径可以使用addPaths()函数来添加

//example
涉及到的头文件
    #include <QFileSystemWatcher>	//文件系统检测器
    #include <QDir>
创建相关的对象
    QFileSystemWatcher myWatcher;
需要被调用的槽函数
    private slots:
		void showMessage(const QString &path);
/*mainwindow.cpp*/    
	搭建信号槽
        connect(&myWatcher,&QFileSystemWatcher::directoryChanged,this,&MainWindow::showMessage); //★目录改变
        connect(&myWatcher,&QFileSystemWatcher::fileChanged,this,&MainWindow::showMessage); //★文件改变
	显示当前目录下的所有.h文件
		QDir myDir(QDir::currentPath());	//创建目录对象，在QDir::currentPath()路径下创建目录
		mydir.setNameFilters(QStringList("*.h"));
		ui->listWidget.addItem(myDir.absolutePath() + tr("目录下的.h文件有:"));
		ui.listWidget.addItems(myDir.entryList()); //myDir.entryList():返回目录中所有文件和目录的名称列表

    创建目录，并将其加入到监视器中
		myDir.mkdir("mydir"); //在QDir::currentPath()路径下创建目录，名称为mydir
		myDir.cd("mydir");  //进入上面创建的目录中
		ui->listWidget->addItem(tr("监视的目录:") + myDir.absolutePath()); //监视这个目录
		myWatcher.addPath(myDir.absolutePath()); //★把这个目录加入到监视器中，代表被监视了

	创建文件，并将其加入到监视器中
        QFile file(myDir.absolutePath() + "/myfile.txt");
		if (file.open(QIODevice::WriteOnly)) {
            QFileInfo info(file);
            ui->listWidget->addItem(tr("监视的文件:") + info.absoluteFilePath()); //主要是为了获取文件的绝对路径
            myWatcher.addPath(info.absoluteFilePath()); //★把这个文件加入到监视器中，代表被监视了
            file.close();
        }
	//如果改变的槽函数
	void showMessage(const QString &path) 
    {
        QDir dir(QDir::curentPath() + "/mydir");
        
        if (path == dir.absolutePath()) {
            ui->listWidget->addItem(dir.dirName() + tr("目录发生改变:"));
            ui->listWidget->addItems(dir.entryList());
        } else {
            ui->listWidget->addItem(path + tr("文件发生改变!"));
        }
    }
```



#### 1.6QString使用技巧

```c++
 /*关键类QString:用于处理字符串，字符串与数值之间的转换，使用QLineEdit就可以实现数字量的输入与输出
    界面设计使用最多的组件QLabel和QLineEdit
        QLabel:用于显示字符串
        QLineEdit:用于显示和输入字符串
    用于读取和设置显示文字的函数：
            QString text() const:用于读取文字
            void setText(const QString &):用于设置显示文字

    1.普通数值与字符串之间的转换
    QString类从字符串转换为整数的函数有：(这些函数如果不设置参数，缺省表示从十进制表示的字符串转换为整数；若指定整数基参数，可以直接将二进制、十六进制字符串转换为整数)
    int toInt(bool *ok = Q_NULLPTR,int base = 10)   const
    long toLong(bool *ok = Q_NULLPTR,int base = 10) const
    short toShort(bool *ok = Q_NULLPTR,int base = 10) const
    uint toUInt(bool *ok = Q_NULLPTR,int base = 10) const
    ulong toULong(bool *ok = Q_NULLPTR,int base = 10) const

    QString类从字符串转换为浮点数的函数有:
    double toDouble(bool *ok = Q_NULLPTR) const;
    float toFloat(bool *ok = Q_NULLPTR) const;

    QString转换为浮点数后希望显示两位小数的方法：
    str = QStirng::number(total,'f',2);     //静态函数，与printf()相反，从后往前，这个先写变量名，在写字符类型，在写保留几位，3个参数
    str = QString::asprintf("%.2f",total);  //静态函数，与C语言的printf()格式一样，2个参数
    str = str.setNum(total,'f',2);          //公共函数，与printf()相反，从后往前，这个先写变量名，在写字符类型，在写保留几位，3个参数
    str = sprintf("%.2f",total);            //公共函数，与C语言的printf()格式一样，2个参数


    2.进制转换
    将一个整数转换为不同进制的字符串，可以使用QStirng的函数setNum()或静态函数number(),他们的函数原型是
    QString &setNum(int n,int base = 10) //n是待转换的整数，base是使用的进制，缺省为10进制，也可以指定为16进制
    QString number (int n,int base = 10)


    3.QString的常用功能
    QString字符串采用的UniCode码（统一码），每一个字符都是一个16位的QChar,而不是8位的char,所以QString处理中文字符没有问题，而且一个汉字算是一个字符。
        1.append()和prepend()
            append();在字符串的后面添加字符串
            prepend();在字符串的前面添加字符串

        2.toUpper()和toLower()
            toUpper():将字符串内的字母全部转换为大写形式
            toLower():将字符串内的字母全部转换为小写形式

        3.count()、size()、length()
            以上三个都返回字符串的字符个数，这3个函数是相同的，但是要注意，字符串中如果有汉字，一个汉字算一个字符

        4.trimmed()和simplified()
            trimmed():去掉字符串首尾的空格
            simplified():不仅去掉首尾的空格，中间连续的空格也用一个空格替换

        5.indexOf()和lastIndexOf()
            indexOf()函数的原型为：int indexOf(const QString &str,int from = 0,Qt::CaseSensitivity cs = Qt::CaseSensitive) const
            功能：在自身字符串内查找参数字符串str出现的位置，参数from是开始查找的位置，Qt::CaseSensitivity cs参数指定是否区分大小写。
            lastIndexOf()函数则是查找某个字符串最后出现的位置

        6.isNull()和isEmpty()
        两个函数都判读字符串是否为空，但是稍有差别，如果一个空字符串，只有"\0",isNull()返回false,而isEmpty()返回true,只有未赋值的字符串，isNull才返回true
        可以这么理解isNull（）主要判断当前的字符串是否仅是未指向任何地址的一个变量，而isEmpty判断当前的字符串是否是一个未指向任何地址的变量或指向了一个""的变量
        QString只要赋值，就在字符串的末尾自动加上"\0"，所以，如果只是要判断字符串内容是否为空，常用isEmpty()

        7.contains()
        判断字符串内是否包含某个字符串，可指定是否区分大小写

        8.startsWith()和endsWith()
        startsWith()判断是否以某个字符串开头，endsWith()判断是否以某个字符串结束

        9.left()和right()
        left()表示从字符串中取左边多少个字符，right表示从字符串中取右边多少个字符，注意，一个汉字被当作一个字符

        10.section()
        函数原型：QString section(const QString &sep,int start,int end = -1,SectionFlags flags = SectionDefault) const
        功能：从字符串中提取以sep作为分隔符，从start端到end端的字符串

    */

//// append()和prepend（）实例
//    QString str1 = "卖";
//    QString str2 = "买";
//    QString str3 = str1;
//    str1.append(str2); //在str1的后面添加字符串str2
//    qDebug() << str1;
//    str3.prepend(str2); //在str3的前面添加字符串str2
//    qDebug() << str3;


////  toUpper()和toLower()实例
//    QString str1 = "Hello,World!",str2,str3;
//    str2 = str1.toUpper(); //str1本身不会发生改变，只不过是把str1存储的字符串转换为大写给到了str2
//    qDebug() << str2;

//    str3 = str1.toLower();
//    qDebug() << str3;

////  count(),size(),length()
//    QString str1 = "Ni好";
//    int A = str1.count();
//    int B = str1.size();
//    int C = str1.length();
//    qDebug() << "A = " << A;
//    qDebug() << "B = " << B;
//    qDebug() << "C = " << C;

////  trimmed()和simplified()
//    QString str1 = "        Are     you OK?   ",str2,str3;
//    str2 = str1.trimmed(); //去掉字符串首尾的空格，中间的空格不作处理
//    qDebug() << str2;

//    str3 = str1.simplified(); //不仅去掉字符串首尾的空格，中间连续的空格也用一个空格替换
//    qDebug() << str3;

////  indexOf()和lastIndexOf()
//    QString str1 = "G:\\Qt5Book\\Qt5.9Study\\qw.cpp"; //“\”是转义字符
//    int A = str1.indexOf("5.9");
//    qDebug()<< A;
//    int B = str1.lastIndexOf("\\"); // "\"是转义字符，如果要查找"\",需要输入"\\"
//    qDebug() << "B = " << B;

////  isNull()和isEmpty()
//    QString str1;
//    QString str2 = "";
//    bool a = str1.isNull(); //ture
//    bool b = str1.isEmpty();//ture
//    bool c = str2.isNull(); //false
//    bool d = str2.isEmpty();//ture
//    qDebug() << a << b << c << d;

////  cotains()
//    QString str1 = "G:\Qt5Book\Qt5.9study\qw.cpp";
//    bool a = str1.contains(".cpp",Qt::CaseInsensitive); //不区分大小写，a = true
//    bool b = str1.contains(".CPP",Qt::CaseSensitive); //区分大小写，b = false
//    qDebug() << "a = " << a << "," << " b = " << b << endl;

////  startsWith()和endsWith()
//    QString str1 = "G:\Qt5Book\Qt5.9study\qw.cpp";
//    bool a = str1.startsWith("g:"); //false
//    bool b = str1.endsWith(".cpp",Qt::CaseInsensitive); //true
//    bool c = str1.endsWith(".CPP",Qt::CaseSensitive); //false
//    qDebug() << a << b << c << endl;

////  left()和right()
//    QString str2 , str3, str1 = "学生姓名，男，1984-3-4，汉族，山东";
//    int n = str1.indexOf("，");
//    str2 = str1.left(n); //学生姓名
//    qDebug() << str2 << endl;
//    int l = str1.lastIndexOf("，");
//    str3 = str1.right(str1.size()-l-1); //山东
//    qDebug() << str3 << endl;

////  section()
//    QString str2,str3,str4,str5,str1 = "学生姓名,男,1984-3-4,汉族,山东";
//    str2 = str1.section(",",0,0);
//    str3 = str1.section(",",1,1);
//    str4 = str1.section(",",0,1);
//    str5 = str1.section(",",4,4);
//    qDebug() << str2 <<endl << str3 << endl << str4 << endl << str5 << endl;

////  字符串分割split()和组合join()
//	  QString str = "Hi,my,,Qt";
//    QStringList list = str.split(",",QString::SkipEmptyParts); //QString::SkipEmptyParts表示跳过空的项目
//    qDebug() << QObject::tr("str拆分后为：") << list;
//    str = list.join(" "); //将各个字符串组合成一个字符串，中间用" "隔开
//    qDebug() << QObject::tr("list组合后为：") << str;

////  字符串查询操作
//	  QString str = "yafeilinux";
//	  qDebug() << "包含右侧5个字符的子字符串：" << str.right(5); 
//	  qDebug() << "包含左侧5个字符的子字符串：" << str.left(5); 
//	  qDebug() << "包含第2个字符以后3个字符的字符串: " << str.mid(2,3);
//	  qDebug() << "'fei'的位置:" << str.indexOf("fei");
//	  qDebug() << "str是否以'ya'开始" << str.startsWith("ya");
//	  qDebug() << "str是否以'linux'结束" << str.endsWith("linux");
//	  qDebug() << "str是否包含'lin'字符串" << str.contains("lin");
////字符串比较
//	  QString str1 = "hello";
//	  if (str1 > str)
//    	qDebug() << str1;
//	  else
//    	qDebug() << str;

//// 字符串转换
QString str = "100";
qDebug() << QObject::tr("字符串转换为整数:") << str.toInt(); //结果为100
int num = 45;
qDebug() << QObject::tr("整数转换为字符串:") << QString::number(num); //整数转换为字符串，结果为"45"
str = "FF";
bool ok;
int hex = str.toInt(&ok,16); //将字符串中的数据转换为16进制,默认为10进制，如果想转换非10进制，需要写bool ok和toInt(&ok,16)
qDebug() << "ok = " << ok << QObject::tr("转换为十六进制:") << hex;
num = 26;
qDebug() << QObject::tr("使用十六进制整数转换为字符串:") << QString::number(num,16);
str = 123.456;
qDebug() << QObject::tr("字符串转换为浮点型:") << str.toFloat();
str = "abc";
qDebug() << QObject::tr("转换为大写:") << str.toUpper();
str = "ABC";
qDebug() << QObject::tr("转换为小写:") << str.toLower();

////arg的用法
    int age = 25;
    QString name = "yafei";
    // name代替%1，age代替%2
    str = QString("name is %1, age is %2").arg(name).arg(age);
    // 结果为name is yafei, age is 25
    qDebug() << QObject::tr("更改后的str为：") << str;
    str = "%1 %2";
    qDebug() << str.arg("%1f","hello");      // 结果为%1f hello
    qDebug() << str.arg("%1f").arg("hello"); // 结果为hellof %2
    str = QString("ni%1").arg("hi",5,'*');
    qDebug() << QObject::tr("设置字段宽度为5，使用'*'填充：") << str;//结果为ni***hi
    qreal value = 123.456;
    str = QString("number: %1").arg(value,0,'f',2);
    qDebug() << QObject::tr("设置小数点位数为两位：") << str;  //结果为"number:123.46
    // 执行下面一行代码，结果为number:123.46不会显示引号
    qDebug() << QObject::tr("将str转换为const char* :") << qPrintable(str);


```

#### 1.7 应用程序主窗口

主窗口：菜单栏、工具栏、状态栏、中心区域

![MainWidget](C:\Users\Gaopeng\Pictures\Saved Pictures\MainWidget.png)

![y应用程序主窗口界面](C:\Users\Gaopeng\Pictures\Saved Pictures\y应用程序主窗口界面.png)

```c++
/*主窗口框架
说明：主窗口为建立应用程序用户界面提供了一个框架，Qt提供了QMainWindow和其他一些相关的类共同完成主窗口的管理
主要：QMainWindow
组件：
	菜单栏(QMenuBar):
		1.菜单栏包含了一个下拉菜单项的列表，这些菜单项由QAction动作类实现
		2.菜单栏位于主窗口的顶部，一个主窗口只能有一个菜单栏
	工具栏(QToolBar):
		1.工具栏一般显示常用的菜单项目，也可以插入其他窗口部件，并且是可以移动的，一个主窗口可以拥有多个工具栏
	中心部件(Central Widget):
		1.在主窗口的中心区域可以放入一个窗口部件作为中心部件，是应用程序的主要功能实现区域
		2.一个主窗口只能拥有一个中心部件
	Dock部件(QDockWidget):
		1.Dock部件常被称为停靠窗口，因为可以停靠在中心部件的四周，用来放置一些部件来实现一些功能，就像个工具箱一样。
		2.一个主窗口可以拥有多个Dock部件
	状态栏(QStatusBar):
		1.状态栏用于显示程序的一些状态信息，在主窗口的最底部
		2.一个主窗口只能拥有一个状态栏
综上：
	1.一个主窗口只能有一个菜单栏，一个中心部件，一个状态栏
	2.一个主串口可以有多个工具栏，多个停靠窗口
	3.带有栏的类名带有"Bar"
	
/*Qt资源系统、菜单栏和工具栏
知识1：ui左上角的"在这里输入"，修改为“文件(&F)”,这里要使用英文半角的括号，“&F”被称为加速键，表明程序运行时可以按下Alt + F 键来激活该菜单，修改完成后按下回车键，并在弹出的下拉菜单中将第一项改为"新建文件(&N)",并按下回车键，
	
```

编码技巧：

```
1.先定义菜单editQMenu，通过菜单栏类的添加菜单addMenu()创建并添加菜单
	QMenu *editmenu = ui->menuBar->addMenu(tr("编辑(&E)")); //核心函数：QMenuBar::addMenu(),返回值QMenu*
2.为菜单创建动作，通过菜单中的addAction()添加动作,核心函数:QMenu::addAction()，返回值QAction*
	QAction *action_Open = editmenu->addAction(QIcon(":/image/images/open.png"),tr("打开文件(&O)"));
3.为工具栏创建动作,核心函数：QToolBar::addAction(),返回值应该也是QAction*
	ui->mainToolBar()->addAction(action_Open);
4.创建动作组，向动作组中添加动作的核心函数:QActionGroup::addAction(),返回值QAction*
	QActionGroup *action_L = new QActionGroup(this); //创建动作组
	QAction *action_L = group->addAction(tr("左对齐(&L)")); //向动作组中添加动作
	action_L->setCheckable(true); //必须设置可以使能，不然无法选中
	QAction *action_R = group->addAction(tr("右对齐(&R)")); 
	action_R->setCheckable(true); //必须设置可以使能，不然无法选中
	QAction *action_C = group->addAction(tr("居中(&C)")); 
	action_C->setCheckable(true); //必须设置可以使能，不然无法选中
	action_L->setChecked(true); //最后指向action_L为选中状态
5.创建QToolButton
	QToolButton *toolBtn = new QToolButton(this);
	toolBtn->setText(tr("颜色"));
6.在创建一个菜单(关于颜色的)
	QMenu *colorMenu = new QMenu(this);
	colorMenu->addAction(tr("红色"));
	colorMenu->addAction(tr("绿色"));
	toolBtn->setMenu(colorMenu);	//QToolButton::setMenu() //想工具按钮中设置菜单
	toolBtn->setPopupMode(QToolButton::MenuButtonPopup); //设置弹出模式(按钮旁边有一个向下的小箭头，可按这个箭头弹菜单)
	ui->mainToolBar->addWidget(toolBtn);                 // 向工具栏添加QToolButton按钮	QToolBar::addWidget()
7.创建QSpinBox类
    QSpinBox *spinBox = new QSpinBox(this);             // 创建QSpinBox
    ui->mainToolBar->addWidget(spinBox);                // 向工具栏添加QSpinBox部件
8.状态栏显示临时消息，显示2000毫秒即2秒,核心函数：QStatusBar::showMessage()	//临时显示
    ui->statusBar->showMessage(tr("欢迎使用多文档编辑器"), 2000);
9.创建标签，设置标签样式并显示信息，然后将其以永久部件的形式添加到状态栏	//永久显示
    QLabel *permanent = new QLabel(this);
    permanent->setFrameStyle(QFrame::Box | QFrame::Sunken); //QLabel::setFrameStyle()
    permanent->setText("www.qter.org"); //QLabel::setText()
    ui->statusBar->addPermanentWidget(permanent); //QStatusBar::addPermanentWidget() 为状态栏添加标签
```

















#### 1.8 事件系统

前言：在Qt中，事件作为一个对象，继承自QEvent类，常见的有**键盘事件QKeyEvent**、**鼠标事件QMouseEvent**和**定时器事件QTimerEvent**等

事件定义：事件是对各种应用程序需要知道的由应用程序内部或者外部产生的事情或者动作的通称。

事件定义（简单）：应用程序和用户之间的交互过程

#### 1.9 属性系统(property)

```
Qt提供了强大的基于元对象系统的属性系统，可以在运行Qt的平台上支持标准C++编译器
要在一个类中声明属性，该类必须继承自QObject类，而且还要在声明前使用Q_PROPERTY()宏
```

直接示例

```c++
//property
//myClass.h
Q_PROPERTY(QString userName READ getUserName WRITE setUserName
          NOTIFY userNameChanged)
public:
	QString getUserName(){return m_userName;}
	void setUserName(QString userName)
    {
    	userName = m_userName;
    	emit userNameChanged(userName);
    }
signals:
	void userNameChanged(QString);
private:
	QString m_userName;

//主界面widget
//widget.cpp
myClass *my = new myClass(this);
connect(my,&myClass::userNameChanged,this,&Widget::userNameChanged);

my->setUserName("Xiaopeng666888");
qDebug() << "userName:" << my->getUserName();

my->setProperty("property","linux");
qDebug() << "property:" << my->property("property").toString();

my->setProperty("number",10);
qDebug() << "number:" << my-<property("number").toString();

void userNameChanged(QString userName)
{
    qDebug() << "property:" << userName;
}
```

#### 1.10 对象树与拥有权（object tree）

```
Qt中使用对象树(object tree)来组织和管理所有的QObject类及其子类的对象
当创建一个QObject时，如果使用了其他的对象作为其父对象(parent),那么这个QObject就会被添加到父对象的children()列表中；当父对象被销毁时，这个QObject也会被销毁。
这个机制非常适用于管理GUI对象，例如，一个QShortCut（键盘快捷键）对象是相应窗口的一个子对象，当用户关闭这个窗口时，快捷键对象也会被销毁。
```

#### 1.11 QVariant

```c++
QVariant v1(15);
qDebug() << v1.toInt();                     // 结果为15

QVariant v2(12.3);
qDebug() << v2.toFloat();                   // 结果为12.3

QVariant v3("nihao");
qDebug() << v3.toString();                  // 结果为"nihao"

QColor color = QColor(Qt::red);
QVariant v4 = color;
qDebug() << v4.type();                      // 结果为QVariant::QColor
qDebug() << v4.value<QColor>();             // 结果为QColor(ARGB 1,1,0,0)

QString str = "hello";
QVariant v5 = str;
qDebug() << v5.canConvert(QVariant::Int);   // 结果为true
qDebug() << v5.toString();                  // 结果为"hello"
qDebug() << v5.convert(QVariant::Int);      // 结果为false
qDebug() << v5.toString();                  // 转换失败，v5被清空，结果为"0"
```

#### 1.12 QTextCharFormat

```c++
//功能：设置当前行文本的格式 需要使用到QTextCharFormat类，设置它的文本颜色或者文本字体，然后并获取 当前文本的光标，从光标开始位置设置文本的字符格式。

//1.设置文本当前行的颜色
void MainWindow::setInsertTextColor(const QColor &color)
{
    QTextCharFormat fmt; //文本字符格式
    fmt.setForeground(color); //前景色(即字体色)设置为color色
    QTextCursor cursor = ui->infoTextEdit->textCursor(); //获取文本光标
    cursor.mergeCharFormat(fmt); //光标后的文本就用该格式显示
    ui->infoTextEdit->mergeCurrentCharFormat(fmt); //textEdit使用当前的字符格式
}

//2.设置文本当前行的字体
void MainWindow::setInsertTextFont(const QFont &font)
{
    QTextCharFormat fmt; //文本字符格式
    fmt.setFont(font); //字体
    QTextCursor cursor = ui->m_textdisplay->textCursor(); //获取文本光标
    cursor.mergeCharFormat(fmt); //光标后的文本就用该格式显示
    ui->m_textdisplay->mergeCurrentCharFormat(fmt); //textEdit使用当前字符格式
    
}
```

#### 1.13 数据字循环转大小端

```c
//数据字两字节颠倒
for(int i = 0;i<iCont;i++)
{
    quint16 *dataTemp =(quint16*)(void*) pOrignal[i].uData;
    for(int j = 0;j<32;j++)
    {
        dataTemp[j]=qFromBigEndian(dataTemp[j]);
    }
}
```

#### 1.14 CKS校验和算法

```c++
//循环右移
#define ROTATE_RIGHTSHIFT(x,s,n) ((((x) >> ((n)%(s))) & 0xFFFF) | (((x) << ((s) - ((n)%(s)))) & 0xFFFF))
//循环左移
#define ROTATE_LEFTSHIFT(x,s,n) ((((x) << ((n)%(s))) & 0xFFFF) | (((x) >> ((s) - ((n)%(s)))) & 0xFFFF))
quint16 MainWindow::CKSCheck(quint8 *buf, int len) //buf = strInfo.data    3
{
    quint16 *Data = new quint16[len/2];
    memcpy(Data,buf,len);
    unsigned short int RET = 0;
    for(unsigned int i = 0; i < len/2; i++)
    {
        RET ^= ROTATE_RIGHTSHIFT((Data[i]),sizeof(Data[i])*8,i);
    }
    delete [] Data;
    Data = NULL;
    return ROTATE_LEFTSHIFT(RET,sizeof(RET)*8,len/2);
}

//特别说明：len长度不包括CKS校验和所占的数据字，即len = 有效长度 - 2（CKS所占的字节）
```

#### 1.15  获取8位数据的某一位

```
    quint8 value= 172;
    qDebug() << QString::number(value >> 0 &0x1,2) << QString::number(value >> 1&0x1,2) << QString::number(value >> 2&0x1,2) << QString::number(value >> 3&0x1,2) << QString::number(value >> 4&0x1,2)
              <<  QString::number(value >> 5&0x1,2) << QString::number(value >> 6&0x1,2) << QString::number(value >> 7&0x1,2) ;
             打印的分别是 0 1 2 3 4 5 6 7位
```



## 三、拓展专栏

#### 2.1组合/获取位操作（移位法）

组合：

```c++
8位组合成16位操作（8位转16位）：
    将2个8位数据high、low合成一个16位数据data_u16：
   	data_u16 = (high<<8) | low;

8位组合成32位操作（8位转32位）：
    将4个8位数据data_u8[4]合成一个32位数据data_u32：
   	data_u32 = (data_u8[0]<<24)|(data_u8[1]<<16)|(data_u8[2]<<8)|data_u8[3];

16位组合成32位操作（16位转32位）：
    将2个16位数据data_u16[2]合成一个32位数据data_u32：
    data_u32 = (data_u16[0]<<16)|data_u16[1];
```

获取：

```c++
16位获取高低位操作（16位转8位）：
	将一个16位数据data_u16拆分成2个8位数据high、low：
	high = (data_u16 >> 8) & 0xff;	 	//高8位
	low = 	data_u16 	   & 0xff; 		//低8位

32位获取高低位操作（32位转8位）：
    将一个32位数据data_u32拆分成4个8位数据data_u8[4]：
    data_u8[0] = (data_u32 >> 24) & 0xff;	 //高8
    data_u8[1] = (data_u32 >> 16) & 0xff; 	 //次高8 
    data_u8[2] = (data_u32 >> 8)  & 0xff;	//次次高8
    data_u8[3] =  data_u32        & 0xff;	//低8
    //高位在前，低位在后

32位获取高低位操作（32位转16位）	
	将一个32位数据data_u32拆分成2个16位数据data_u16[2]：
    data_u16[0] = (data_u32 >> 16) & 0xffff;	 //高16位
    data_u16[1] =  data_u32        & 0xffff; 	 //低16位
```

#### 2.2 #ifndef #define #endif意义

想必很多人都看过“头文件中的 #ifndef/#define/#endif 防止该头文件被重复引用”。但是是否能理解“被重复引用”是什么意思？是不能在不同的两个文件中使用include来包含这个头文件吗？如果头文件被重复引用了，会产生什么后果？是不是所有的头文件中都要加入#ifndef/#define/#endif 这些代码？

```
其实“被重复引用”是指一个头文件在同一个cpp文件中被include了多次，这种错误常常是由于include嵌套造成的。比如：存在a.h文件#include "c.h"而此时b.cpp文件导入了#include "a.h" 和#include "c.h"此时就会造成c.h重复引用。
```

头文件被重复引用引起的后果：

有些头文件重复引用只是增加了编译工作的工作量，不会引起太大的问题，仅仅是编译效率低一些，但是对于大工程而言编译效率低下那将是一件多么痛苦的事情。有些头文件重复包含，会引起错误，比如在头文件中定义了全局变量(虽然这种方式不被推荐，但确实是C规范允许的)这种会引起重复定义。

```
是不是所有的头文件中都要加入#ifndef/#define/#endif 这些代码？
答案：不是一定要加，但是不管怎样，用#ifnde xxx #define xxx #endif或者其他方式避免头文件重复包含，只有好处没有坏处。个人觉得培养一个好的编程习惯是学习编程的一个重要分支。

下面给一个#ifndef/#define/#endif的格式：

#ifndef A_H意思是"if not define a.h"  如果不存在a.h
接着的语句应该#define A_H  就引入a.h
最后一句应该写#endif   否则不需要引入

example:
#ifndef GRAPHICS_H // 防止graphics.h被重复引用 
#define GRAPHICS_H 

#include <math.h> // 引用标准库的头文件 
… 
#include “header.h” // 引用非标准库的头文件 
… 
void Function1(…); // 全局函数声明 
… 
class Box // 类结构声明 
{ 
… 
}; 
#endif
```

--------------------------------------------------------------------------------------------------


#### 2.3 Qt创建线程返回句柄的方法CreateThread()

线程是进程中的一个实体，是被系统独立调度和分派的基本单位。一个进程可以拥有多个线程，但是一个线程必须有一个进程。线程自己不拥有系统资源，只有运行所必须的一些数据结构，但它可以与同属于一个进程的其它线程共享进程所拥有的全部资源，同一个进程中的多个线程可以并发执行。

在C/C++中可以通过CreateThread函数在进程中创建线程，函数的具体格式如下：

HANDLE CreateThread(
                    LPSECURITY_ATTRIBUTES lpThreadAttributes,
                    DWORD dwStackSize,
                    LPTHREAD_START_ROUTINE lpStartAddress,
                    LPVOID lpParameter,
                    DWORD dwCreationFlags,
                    LPDWORD lpThreadID
                   );
参数的含义如下：
lpThreadAttrivutes：指向SECURITY_ATTRIBUTES的指针，用于定义新线程的安全属性，一般设置成NULL；

dwStackSize：分配以字节数表示的线程堆栈的大小，默认值是0；

lpStartAddress：指向一个线程函数地址。每个线程都有自己的线程函数，线程函数是线程具体的执行代码；

lpParameter：传递给线程函数的参数；

dwCreationFlags：表示创建线程的运行状态，其中CREATE_SUSPEND表示挂起当前创建的线程，而0表示立即执行当前创建的进程；

lpThreadID：返回新创建的线程的ID编号；

如果函数调用成功，则返回新线程的句柄，调用WaitForSingleObject函数等待所创建线程的运行结束。函数的格式如下：

DWORD WaitForSingleObject(
                          HANDLE hHandle,
                          DWORD dwMilliseconds
                         );
参数的含义如下：
hHandle：指定对象或时间的句柄；

dwMilliseconds：等待时间，以毫秒为单位，当超过等待时间时，此函数返回。如果参数设置为0，则该函数立即返回；如果设置成INFINITE，则该函数直到有信号才返回。

一般情况下需要创建多个线程来提高程序的执行效率，但是多个线程同时运行的时候可能调用线程函数，在多个线程同时对一个内存地址进行写入操作，由于CPU时间调度的问题，写入的数据会被多次覆盖，所以要使线程同步。

就是说，当有一个线程对文件进行操作时，其它线程只能等待。可以通过临界区对象实现线程同步。临界区对象是定义在数据段中的一个CRITICAL_SECTION结构，Windows内部使用这个结构记录一些信息，确保同一时间只有一个线程访问改数据段中的数据。

使用临界区的步骤如下：

（1）初始化一个CRITICAL_SECTION结构；在使用临界区对象之前，需要定义全局CRITICAL_SECTION变量，在调用CreateThread函数前调用InitializeCriticalSection函数初始化临界区对象；

（2）申请进入一个临界区；在线程函数中要对保护的数据进行操作前，可以通过调用EnterCriticalSection函数申请进入临界区。由于同一时间内只能有一个线程进入临界区，所以在申请的时候如果有一个线程已经进入临界区，则该函数就会一直等到那个线程执行完临界区代码；

（3）离开临界区；当执行完临界区代码后，需要调用LeaveCriticalSection函数离开临界区；

（4）删除临界区；当不需要临界区时调用DeleteCriticalSection函数将临界区对象删除；

下面的代码创建了5个线程，每个线程在文件中写入10000个“hello”：

```c++
#include <stdio.h>
#include <windows.h>
HANDLE hFile;
CRITICAL_SECTION cs;//定义临界区全局变量
//线程函数：在文件中写入10000个hello
DWORD WINAPI Thread(LPVOID lpParam)
{
    int n = (int)lpParam;
    DWORD dwWrite;
    for (int i = 0;i < 10000;i++)
    {
        //进入临界区
        EnterCriticalSection(&cs);
        char data[512] = "hello\r\n";
        //写文件
        WriteFile(hFile, data, strlen(data), &dwWrite, NULL);
        //离开临界区
        LeaveCriticalSection(&cs);
    }
    printf("Thread #%d returned successfully\n", n);
    return 0;
}
int main()
{
    char *filename = "hack.txt";
    WCHAR name[20] = { 0 };
    MultiByteToWideChar(CP_ACP, 0, filename, strlen(filename) + 1, name, sizeof(name) / sizeof(name[0]));
    //创建文件
    hFile = CreateFile(name, GENERIC_WRITE, 0, NULL, CREATE_ALWAYS, FILE_ATTRIBUTE_NORMAL, NULL);
    if (hFile == INVALID_HANDLE_VALUE)
    {
        printf("CreateFile error.\n");
        return 0;
    }
    DWORD ThreadID;
    HANDLE hThread[5];
    //初始化临界区
    InitializeCriticalSection(&cs);
    for (int i = 0;i < 5;i++)
    {
        //创建线程，并调用Thread写文件
        hThread[i] = CreateThread(NULL, 0, Thread, (LPVOID)(i + 1), 0, &ThreadID);
        printf("Thread #%d has been created successfully.\n", i + 1);
    }
    //等待所有进程结束
    WaitForMultipleObjects(5, hThread, TRUE, INFINITE);
    //删除临界区
    DeleteCriticalSection(&cs);
    //关闭文件句柄
    CloseHandle(hFile);
    return 0;
}
```


结果如图：
![image-20220927142903916](C:\Users\Gaopeng\AppData\Roaming\Typora\typora-user-images\image-20220927142903916.png)

```c++
example2:
    HANDLE m_hdBDSearch;	//创建线程需要返回的句柄
    static void  Thread_BDSearch(LPVOID * pv);	//线程对应的地址函数
    void ThdBDSearch(); //真正的函数

	//LPTHREAD_START_ROUTINE:万能线程_启动_常规
    m_hdBDSearch = CreateThread(NULL, 0, (LPTHREAD_START_ROUTINE)Thread_BDSearch, this, 0, NULL); 
    
    void ControlProcess::Thread_BDSearch(LPVOID * pv) //LPVOID *:万能指针	(LPVOID:void *)
    {
        ControlProcess* p_obj = (ControlProcess*)pv;
        p_obj->ThdBDSearch();
    }
    
    void ControlProcess::ThdBDSearch()
	{
		xxx;
	}

其他操作：
    m_hdBDSearch = INVALAID_HANDLE_VALUE;//初始化句柄

	//关闭句柄操作
	CloseHandle(m_hdBDSearch);
	m_hdBDSearch = INVALAID_HANDLE_VALUE; 
```



#### 2.4 Qt中的QSettings用法

```c++
QString m_CurrPath = QCoreapplication::applicationDirPath(); //exe所在的路径
QString strCfgFilePath = m_CurrPath + "/config/test.ini";
QSettings objIni(strCfgFilePath,QSettings::IniFormat);
objIni.setIniCodec("GBK");
QString strName = objIni.value("/Test/strName").toString();
```

#### 2.5 改变部件大小resize()和设置固定大小

```c++
resize(宽度，高度); //单位像素
setFixSize(宽度，高度); //设置固定大小
```

#### 2.6 通过setupUi()设置Ui

```c++
    QApplication a(argc, argv);
    QDialog w;  //1
    Ui::HelloDialog ui; //2
    ui.setupUi(&w); //关键
    w.show(); //关键4
    return a.exec();
```

#### 2.7 show()和exec()的区别

```c++
1. show()函数：
即可以显示非模态也可以显示模态对话框；
当设置modal为true时，显示模态对话框，
    QDialog::setModal(bool model) ，为 false（默认 false）则表示 Qt::NonModal ，为 true 则表示 Qt::ApplicationModal 

2. exec()函数：
显示模态对话框，不关闭此对话框，不能执行别的操作。

3.区别：
show()函数显示模态对话框时，是否与exec()显示的一样呢？答案是：不一样
show()显示的模态对话框并非真正意义上的模态，虽然在对话框弹出的时候，程序的其它操作（按钮、窗口切换等）都失效了；但是程序仍然在调用对话框之后，马上继续执行后面的代码。这样，就不会得到窗口的返回值。
exec()函数在调用之后，程序就被锁定在原地。等待窗口的关闭。
```

#### 2.8 setWindowState() 设置窗口的状态

```c++
QWidget还有一个setWindowState()函数用来设置窗口的状态，其参数由Qt::WindowStates指定，是Qt::WindowState枚举类型值或组合。窗口状态Qt::WindowState包括最大化Qt::WindowMaximized、最小化Qt::WindowMinimized、全屏显示Qt::WindowFullScreen和活动窗口Qt::WindowActive等，默认值为正常状态Qt::WindowNoState
枚举：
    Qt::WindowNoState     //窗口 正常显示
    Qt::WindowMinimized   //窗口 最小显示
    Qt::WindowMaximized   //窗口 最大显示
    Qt::WindowFullScreen  //窗口 填充整个屏幕，无边框
    Qt::WindowActive      //窗口 变为活动的窗口（如：可接受键盘输入） 
```

#### 2.9 setWindowFlags() 设置窗口属性

```c++
Qt::Widget               //是一个窗口或部件，有父窗口就是部件，没有就是窗口
Qt::Window               //是一个窗口，有窗口边框和标题
Qt::Dialog               //是一个对话框窗口
Qt::Sheet                //是一个窗口或部件Macintosh表单
Qt::Drawer               //是一个窗口或部件Macintosh抽屉，去掉窗口左上角的图标
Qt::Popup                //是一个弹出式顶层窗口
Qt::Tool                 //是一个工具窗口
Qt::ToolTip              //是一个提示窗口，没有标题栏和窗口边框
Qt::SplashScreen         //是一个欢迎窗口，是QSplashScreen构造函数的默认值
Qt::Desktop              //是一个桌面窗口或部件
Qt::SubWindow            //是一个子窗口

this->setWindowFlags(Qt::ToolTip);

Qt::MSWindowFiredSizeDialogHint:     为Windows系统上的窗口装饰一个窄的对话框边框，通常这个提示用于固定大小的对话框
Qt::MSWindowOwnDC:                   为Windows系统上的窗口添加自身的显示上下文菜单
Qt::X11BypassWindowManagerHint:      完全忽视窗口管理器，它的作用是产生一个根本不被管理的无窗口边框的窗口(此时，用户无法使								  用键盘进行输入，除非手动调用QWidget::activateWindow()函数)
Qt::FramelessWindowHint:             产生一个无窗口边框的窗口，此时用户无法移动该窗口和改变它的大小
Qt::CustomizeWindowHint:             关闭默认的窗口标题提示
Qt::WindowTitleHint：                为窗口装饰一个标题栏
Qt::WindowSystemMenuHint:            为窗口添加一个窗口系统系统菜单，并尽可能地添加一个关闭按钮
Qt::WindowMinimizeButtonHint:        为窗口添加一个“最小化”按钮
Qt::WindowMaximizeButtonHint:        为窗口添加一个“最大化”按钮
Qt::WindowMinMaxButtonHint:          为窗口添加一个“最小化”按钮 和一个“最大化”按钮
Qt::WindowContextHelpButtonHint:     为窗口添加一个“上下文帮助”按钮
Qt::WindowStaysOnTopHint:            置顶窗口
Qt::WindowType_Mask:                 一个用于提示窗口标识的窗口类型部分的掩码

this->setWindowFlags(windowFlags()|Qt::FramelessWindowHint );

```

#### 2.9 show()也可以成为模态对话框，setModal()

```c++
QDialog m_dialog = new QDialog(this);
m_dialog.show();
m_dialog.setModal(true); //通过setModal(true) 即m_dialog对话框变成模态的了！！！
//exec()生成的一定是模态对话框，show()默认打开的非模态对话框
//虽然show()通过setModal()也呈现出了模态对话框的效果，但是与exec()还是有区别的
//区别：调用完show()函数后会立即将控制权交给调用者，程序可以继续往下执行。
//而调用exec()函数却不同，只有当对话框被关闭时才会返回
//与setModal()函数相似的还有一个setWindowModality()函数，他有一个参数来设置模态对话框要阻塞的窗口类型，可以是
//Qt::NonModal(不阻塞任何窗口，就是非模态)、Qt::WindowModal(阻塞它的父窗口，所有祖先窗口以及它们的子窗口)
//或Qt::ApplicationModal(阻塞整个应用程序的所有窗口)。而setModal()函数默认设置的是Qt::ApplicationModal
```

#### 2.10 Qt4和Qt5使用信号槽的区别（Qt5发生重载时重点注意）

```c++
//示例：
signals:
  testSignalOne();
  testSignalOne(int params);
  testSignal(int params);
 
piblic slots:
  testSlotOne();
  testSlotOne(int params);
  testSlot(int params);

QT4信号连接
 (1) 槽函数必须有slots关键字
 (2) SIGNAL SLOT将函数转为字符串，不进行错误检查
 (3) 槽函数和信号一致(参数，返回值)，没有返回值
 connect(this, SIGNAL(testSignalOne()), this, SLOT(testSlotOne()));
 connect(this, SIGNAL(testSignalOne(int)), this, SLOT(testSlotOne(int)));

 Qt5信号连接
 (1) SIGNAL SLOT会进行错误检查
 (2) 槽可以是任意的成员函数，普通全局函数和静态函数
 (3) 槽函数和信号一致(参数，返回值)，没有返回值

 //重载情况下使用 函数指针
 void (MyWidget::*signalOne)() = &MyWidget::testSignalOne;
 void (MyWidget::*slotOne)() = &MyWidget::testSlotOne;
 connect(this, signalOne, this, slotOne);

 void (MyWidget::*signalTwo)(int) = &MyWidget::testSignalOne(int);
 void (MyWidget::*slotTwo)(int) = &MyWidget::testSlotOne(int);
 connect(this, signalTwo, this, slotTwo);


 // 非重载可以直接使用
 connect(this, &MyWidget::testSignal, this, &MyWidget::testSlot);

 this 信号发送者
 &MyWidget::testSignal 处理的信号，格式为，&发送者的类名::信号名字

 this 信号接收者
 &MyWidget::testSlot 槽函数，信号处理函数，格式为，&接收者的类名::信号名字
 

```

#### 2.11 自定义对话框之exec()与QDialog::Accept的故事

```c
//accept()函数
//这个accept()函数是QDialog类中的一个槽，对于一个使用exec()函数实现的模态对话框，执行了这个槽就会隐藏这个模态对话框，并返回QDialog::Accepted值，这里就是要使用这个值来判断是哪个按钮被按下了。与其对应的还有个reject()槽，它可以返回一个QDialog::Rejected值，前面的"退出程序"按钮也可以关联这个槽。
```

#### 2.12 QFont之setBold()、setItalic()、setPointSize()、setFamily()

```c++
//example:
	QFont font;
	font.setFamily("华文行楷"); //设置字体族
	font.setPointSize(20); //设置字体大小
	font.setBold(true); //设置字体加粗
	font.setItalic(true); //设置字体斜体
```

#### 2.13 QDateTime

```c++
ui->dateTimeEdit	类名：QDateTimeEdit
ui->dateTimeEdit->setDateTime(QDateTime::currentDateTime()); //设置当前时间	
ui->dateTimeEdit->setDisplayFormat(r("yyyy年MM月dd日ddd HH时mm分ss秒"))
```

#### 2.14 QLineEdit

```c++
ui->lineEdit->text(); //输出lineEdit的内容
ui->lineEdit->displayText(); //输出lineEdit显示的内容
```

#### 2.15 QDateTimeEdit

```c++
ui->dateTimeEdit->setDateTime(QDateTime::currentDateTime());
ui->dateTimeEdit->setDisplayFormat("yyyy年MM月dd日 HH时mm分ss秒");
```

#### 2.16 QWidget::inherits()判断父类是什么类型

```c++
QWidget *MyAction::createWidget(QWidget *parent)
{
	if(parent->inherits("QMenu")){
		qDebug() << "current Widget is QMenu" << endl;
	}else if(patent->inherits("QToolBar")){
		qDebug() << "current Widget is QToolBar" << endl;
	}else{
		qDebug() << "cureent Widget is other Widget" << endl;
	}
}
```

#### 2.17 QSplitter 拆分器

```c++
QSplitter *splitter = new QSplitter(this);
QLabel *label = new QLabel;
label->setText(tr("插入文本:"));
splitter->addWidget(label);
splitter->addWdget(ui->lineEdit);
return splitter;
```

#### 2.18 按下回车对应的信号QLineEdit::returnPressed

```c++
//说明:QLineEdit::returnPressed代表按下回车的信号 可参考5-2 myAction
```

#### 2.19 设置字符串编码

```c++
QTextCodec::setCodecForTr(QTextCodec::codecForName("UTF-8"));   QTextCodec::setCodecForCStrings(QTextCodec::codecForName("UTF-8"));
```

#### 2.20 this->update()

```
项目中需要通过设置来更新界面（即 paintEvent(QPaintEvent *）），这个过程中若是窗口没有发生变化，即使通过调用update()函数来触发重绘函数重绘窗口，也不能立即显示被重绘的窗口。只有窗口变化的时.候才会被显示出来。
所以可以通过定时调用 update（）调用绘图事件来实现画面更新
```

#### 2.21 函数后面加const

```
函数后面加const关键字，这告诉编译器，该函数不会改变成员变量的值（因为是成员变量，所以只有类或结构体的成员函数才能加const函数）。
也让阅读代码的人一眼看就知道这个函数不会改变成员的值，有利于代码可读性。
一般情况下，函数不改变成员变量的值，也可以不加const，但是在某些情况下必须加，比如：
用到sort函数对类或结构体进行排序时，需要自定义比较函数或者重载<运算符，如果选择重载运算符，那么这个重载运算符函数后面必须加const，否则就算你重载了这个运算符，也会说找不到合适的函数，这是sort函数的规定。
所以不改变成员变量的成员函数最好加const，必须加const则是因为调用某些函数时，那个函数要求提供一个带const的函数。
```

#### 2.22 位运算(&,|,^,...)

```
位运算概览
符号	描述	运算规则
&	与	两个位都为1时，结果才为1
|	或	两个位都为0时，结果才为0
^	异或	两个位相同为0，相异为1
~	取反	0变1，1变0
<<	左移	各二进位全部左移若干位，高位丢弃，低位补0
>>	右移	各二进位全部右移若干位，对无符号数，高位补0，有符号数，各编译器处理方法不一样，有的补符号位（算术右移），有的补0（逻辑右移）
```

#### 2.23 Qt命名空间开始结束宏（常见于xxx_ui.h中）

```
QT_BEGIN_NAMESPACE	//Qt命名空间开始宏
QT_END_NAMESAPCE	//Qt命名空间结束宏
```

#### 2.24 设置对象名称

```c++
void setupUi(QDialog *dg1)
{
	QLabel *label;
	if (dg1->objectName().isEmpty())
		dg1->setObjectName(QString::fromUtf8("dg1")); //设置对话框的对象名称
	dg1->resize(200,100);
    label = new QLabel(dg1);
    label->setObjectName(QString::fromUtf8("label")); //设置标签的对象名称
    label->setGeometry(QRect(60,50,52,14));
}
```

#### 2.25 xxx_ui.h文件分析

```c++
/********************************************************************************
** Form generated from reading UI file 'dg.ui'
**
** Created by: Qt User Interface Compiler version 5.12.4
**
** WARNING! All changes made in this file will be lost when recompiling UI file!
********************************************************************************/

#ifndef UI_DG_H		//#ifndef #define #endif 预处理器用于防止头文件被重复包含
#define UI_DG_H

#include <QtCore/QVariant>			//包含了一系列的头文件
#include <QtWidgets/QApplication>
#include <QtWidgets/QDialog>
#include <QtWidgets/QLabel>

QT_BEGIN_NAMESPACE	//Qt的命名空间开始宏

class Ui_dg1	//定义一个类
{
public:
    QLabel *label;	//添加到对话框的标签
    
//此函数用于生成界面，程序必须调用此函数，才能产生出界面，也就是说，虽然设计模式能拖放出界面的外观，但还是要编写代码来调用此函数以生成界面。
    void setupUi(QDialog *dg1) 
    {
        if (dg1->objectName().isEmpty())
            dg1->setObjectName(QString::fromUtf8("dg1")); //设置对话框的对象名称
        dg1->resize(400, 300); //设置对话框的大小
        label = new QLabel(dg1); //将标签添加到对话框之上
        label->setObjectName(QString::fromUtf8("label")); //设置标签的对象名称
        label->setGeometry(QRect(90, 90, 72, 15)); //设置标签的位置和大小

        retranslateUi(dg1);

        QMetaObject::connectSlotsByName(dg1); //主要用于实现信号和槽的关联
    } // setupUi

    void retranslateUi(QDialog *dg1)
    {
        dg1->setWindowTitle(QApplication::translate("dg1", "Dialog", nullptr));
        label->setText(QApplication::translate("dg1", "TextLabel", nullptr));
    } // retranslateUi

};

namespace Ui {
    class dg1: public Ui_dg1 {};
} // namespace Ui

QT_END_NAMESPACE	//QT的命名空间结束宏

#endif // UI_DG_H

```



## 四、题外专栏

#### 3.1 Qt强大的对象模型

```c++
一个强大的无缝对象通信机制---信号和槽(signals and slots)	--- connect()
可查询、可设计的对象属性系统(object properties)
强大的事件和事件过滤器(events and event filter) 
基于上下文的国际化字符串翻译机制(string translation for internationalization)	---tr()
完善的定时器(timers)驱动，可以再一个事件驱动的GUI中处理多个任务
分层结构的、可查询的对象树(object trees)，它使用一种很自然的方式来组织对象拥有权(object ownership)
守卫指针即QPointer,它在引用对象被销毁时自动将其设置为0
动态的对象转换机制(dynamic cast);
支持创建自定义类(custom type);
```

综上：

​	1.Qt的这些特性都是在遵循标准C++规范内实现的

​	2.使用这些特性都必须要继承自QObject类

​	3.对象通信机制（信号槽）和动态属性系统还需要元对象系统(Meta-Object System)的支持

#### 3.2 什么是回调?(callback)

```
回调定义：
	回调就是指向函数的指针，把这个指针传递给一个要被处理的函数，那么就可以在这个函数被处理时在适当的地方调用这个回调函数。
回调缺陷：
	不是类型安全的，不能保证在调用回调函数时可以使用正确的参数
	是强耦合的，处理函数必须知道调用哪个回调函数
```

#### 3.3 多信号关联多槽的执行顺序

```
一个信号可以关联多个槽
多个信号可以关联多个槽
一个信号可以关联另一个信号
如果存在多个槽与某个信号关联，那么当这个信号被发射时，这些槽将会一个接一个地执行，执行顺序与关联顺序相同
```

#### 3.4 信号槽注意事项

```c++
声明一个信号要使用signals关键字，在signals前面不能用public、private和protected等限定符，因为信号默认是public函数，可以从任何地方发射，但是建议只在定义该信号的类及其子类中发射该信号
信号只用声明，不需要也不能对它进行定义实现，且返回值为void类型
信号没有返回值，只能是void类型，因为只有QObject类及其子类派生的类才能使用信号和槽机制（需要继承自QObject或其子类）
使用信号和槽必须在类声明的最开始处添加Q_OBJECT宏(在类声明最开始处添加Q_OBJECT宏)
槽也可以被声明为虚函数，这与普通的成员函数是一样的
槽最大的特点就是可以和信号关联
槽中参数的类型要和信号参数的类型相对应，且不能比信号的参数多
connect(&sender,SIGNAL(sendFunc(int)),&receive,SLOT(recFunc(int))); //SIGNAL()和SLOT()中的函数参数不能有具体变量名，比如connectconnect(&sender,SIGNAL(sendFunc(int ivalue)),&receive,SLOT(recFunc(int ivalue)))就是不对的，不能写ivalue参数
Lambda表达式写法（精简代码建议使用）：connect(dlg,&MyDialog::dlgReturn,[=](int ivalue){
		ui->label->setText(tr("获取的值是:%1").arg(ivalue));								
});
信号和槽的3中写法
	写法1：connect(sender,SIGNAL(sendFunc(int)),receive,SLOT(recFunc(int)));
	写法2：connect(sender,QPushButton::clicked,sender,QWidget::close);
	写法3: on_pushButton_clicked() //由字符串on、部件的objectName、信号名称3部分组成，中间用下划线隔开，这种形式命名的槽可以直接和信号关联，不用再使用connect()函数，这个部件的objectName一定要通过setObjectName()设置一下,如
	QPushButton *btn = new QPushButton(this); //创建按钮
	btn->setObjectName("myButton"); //指定按钮的对象名
	ui->setupUi(this); //要在定义了部件以后再调用这个函数，因为setupUi()函数调用了connectSlotsByName()函数，所以要使用自	   动关联的部件的定义都要放在setupUi()函数调用之前，而且还必须使用setObjectName()指定他们的objectName,只有这样才能正常使用自动关联 
```

#### 3.5 信号槽断开关联

可以通过disconnect()函数来断开信号和槽的关联，其原型如下：

```
[static]bool QObject::disconnect(const QObject *sender,const char *signal,
								const QObject *receiver,const char *method);
```

该函数一般的写法:

```
断开与一个对象所有信号的所有关联：
	方法1：disconnect(myObject,0,0,0);
	方法2：myObject->disconnect();
断开与一个指定信号的所有关联：
	方法1：disconnect(myObject,SIGNAL(mysignal()),0,0);
	方法2：myObject->disconnect(SIGNAL(mysignal()));
断开与一个指定的receiver的所有关联:
	方法1：disconnect(myObject,0,myReceiver,0);
	方法2：myObject->disconnect(myReceiver);
断开一个指定信号和槽的关联
	方法1：disconnect(myObject,SIGNAL(mysignal()),myReceiver,SLOT(mySlot()));
	方法2：myObject->disconnect(SIGNAL(mysignal()),myReceiver,SLOT(mySlot()));
	方法3：disconnect(myConnection); //myConnection是进行关联时connect()的返回值
```

## 五、师夷长技以制夷

#### Qt容器类(container class)

```c++
Qt提供了一组通用的基于模板的容器类(container classes),这些容器可以用来存储指定类型的项目（items）；例如，如果需要一个QString类型的大小可变的数组，那么可以使用QVector<QString>
Qt提供了一些顺序容器：一个接一个线性存储的，所以称为顺序容器,如QList、QLinkedList、QVector、QStack、QQueue，对于大多数应用程序而言，使用最多而且最好用的是QList,尽管它是一个数组列表，但是可以快速在其头部和尾部进行添加操作，如果需要使用一个链表，那么可以使用QLinkedList;如果希望数据项可以占用连续的内存空间，那么可以使用QVector。而QStack和QQueue分别提供了后进先出（LIFO）和先进先出(FIFO)语义。
Qt提供了一些关联容器：关联容器存储的是<键，值>对，QMap、QMultiMap、QHash、QMultiHash和QSet，其中Multi容器用来支持一个键多个值的情况。
Qt提供了一些其他容器：提供对缓存存储中对象的高效散列查找，如QCache和QContiguousCache
```

##### ![](C:\Users\Gaopeng\Pictures\Saved Pictures\Container.png)

![Container_2](C:\Users\Gaopeng\Pictures\Saved Pictures\Container_2.png)

##### QList<T>

```c++
QList是一个模板类，它提供了一个列表。
QList<T>实际上是一个T类型项目的指针数组，所以它支持基于索引的访问，而且当项目的数目小于1000时，可以实现在列表中间进行快速地插入操作。
QList提供了很多方便的接口函数来操作列表中的项目
	插入操作：insert()
	替换操作: replace()
	移除操作: removeAt() //未实践	list.remove(index)
	移动操作: move() //未实践	list.move(from,to)
	交换操作: swap()
	表尾添加项目: append()
	表头添加项目: prepend()
	移除第一个项目: removeFirst() //未实践
	移除最后一个项目：removeLast() //未实践
	从列表中移除一项并获取这个项目: takeAt()、takeFirst()、takeLast()
	获取一个项目的索引: indexOf() 
	判断是否含有相应的项目: contains()
	获取一个项目出现的次数: count()
	特殊操作：
		QList可以使用"<<"操作符向列表中插入项目
		QList可以使用"[]"操作符通过索引来访问一个项目，其中项目是从0开始编号的
		QList可以使用at()函数来访问一个项目，它比"[]"操作符要快很多（只对于只读的访问）
```

Example

```c++
#include <QList>
QList<QString> list;
//插入项目
list << "aa" << "bb" << "cc";	// <<
//赋值操作
if(list[1] == "bb"){
    list[1] = "ab";	// list[index] = "string";
}
//替换操作
list.replace(2,"bc"); //list.replace()
//打印输出整个列表
qDebug() << "the list is: ";
for(int i=0; i<list.size(); i++){
    qDebug() << list.at(i); //list.at()
}
//在列表尾部添加元素
list.append("dd"); //list.append()
//在列表头部添加元素
list.prepend("mm"); //list.prepend()
//从列表中删除第三个项目并获取它
QString string = list.takeAt(2); //list.takeAt()
qDebug() << "At(2) item is: " << string;
//打印输出整个列表
qDebug() << "the list is: ";
for(int i=0; i<list.size(); i++){
    qDebug() << list.at(i);
}
//在位置2插入元素
list.insert(2,"mm"); //list.insert()
//交换元素1和元素3
list.swap(1,3); //list.swap()
//打印输出整个列表
qDebug() << "the list is: ";
for(int i=0; i<list.size(); i++){
    qDebug() << list.at(i);
}
//判断列表中是否包含"mm"
qDebug() << "contains 'm' ?" << list.contains("mm"); //list.contains()
//包含"mm"的个数
qDebug() << "the 'mm' count: " << list.count("mm"); //list.count()
//第一个mm的位置，默认从位置0开始往前查找，返回第一个匹配的项目的位置
qDebug() << "the first 'mm' index: " << list.indexOf("mm"); //list.indexOf()
//第二个mm的位置，我们指定从位置1往后查找
qDebug() << "the second 'm' index: " << list.indexOf("mm",1); //list.indexOf()
//删除第0个元素
list.removeAt(0)
```

```tex
小技巧：
	1.QList存储的数据可以直接打印出来
		QList<int> list;
		list << 1 << 2 << 3;
		qDebug() << "the list is: " << list; //the list is (1,2,3)
```



##### QMap<T>

```
QMap是一个容器类，它提供了一个基于跳跃列表的字典（a skip-list-based dictionary）
QMap<Key,T>是Qt的通用容器之一，它存储（键，值）并对提供了与键相关的值的快速查找
QMap中提供了很多方便的接口函数：
	插入操作：insert()
	获取值: value()
	是否包含了一个键: contains()
	删除一个键: remove()
	删除一个键并获取该键对应的值: take()
	清空操作: clear()
	插入一键多值: insertMulti()
	特殊操作：
		可以使用"[]"操作符插入一个键值对或者获取一个键的值，不过当使用该操作符获取一个不存在的键的值时，会默认向map插入该键，为了避免这个情况，可以使用value()函数来获取键的值，当使用value()函数时，如果指定的键不存在，那么默认会返回0，可以在使用该函数时提供参数来更改这个默认返回的值。QMap默认是一个键对应一个值的，但是也可以使用insertMulti()进行一键多值的插入；对于一键多值的情况，更方便的是使用QMap的子类QMultiMap
容器也可以嵌套使用，比如QMap<QString,QList<int> >,这里键的类型是QString,而值的类型是QList<int>,注意后面的"> >"符号之间要有一个空格，不然编译器会将它作为">>"操作符对待，各种容器存储的值的类型可以是任何的可赋值的数据类型，该类型需要有一个默认的构造函数，一个复制构造函数和一个赋值操作运算符，像基本的类型（如int何double）、指针类型、Qt的数据类型（如QString和QDate等），但不包括QObject以及QObject的子类(QWidget、QDialog、QTimer等)，不过可以存储这些类的指针，如QList<QWidget *>,也可以自定义数据类型，具体方法可以参考Container Classes文档中的相关内容
```

Example

```c++
#include <QMap>
#include <QMultiMap>

QMap<QString,int> map;
//直接写键值
map["one"] = 1;
map["three"] = 3;
//通过insert()赋值
map.insert("seven",7);
//获取值
//方法1：直接获取
int value1 = map["six"];
qDebug() << "value1 = " << value1;
qDebug() << "contains 'six' ?" << map.contains("six");
//方法2：通过value()获取
int value2 = map.value("five");
qDebug() << "five = " << value2;
qDebug() << "contains 'five' ?" << map.contains("five");
//当键不存在时，value默认返回0，这里可以设定该值，比如这里设置9
int value3 = map.value("nine",9);
qDebug() << "value3: " << value3;
//map是一个键对应一个值，如果重新给该键设置了值，那么以前的会被擦除
map.insert("ten",10); //第一次
map.insert("ten",100); //第二次
qDebug() << "ten = " << map.value("ten"); //100
//可以使用insertMulti()函数来实现一键多值，然后使用values()函数来获取值的列表
map.insertMulti("two",2);
map.insertMulti("two",200);
QList<int> values = map.value("two");
qDebug() << "two = " << values;
//可以使用QMultiMap来实现一键多值 定义可以一键生成多个map
QMultimap<QString,int> map1,map2,map3;
map1.insert("values",1);
map1.insert("values",2);
map2.insert("values",3);
//QMultiMap可以相加
map3 = map1 + map2;
QList<int> myValue = map3.values("values");
for(int i=0; i<myValue.size(); i++){
    qDebug() << "values = " << myValue.at(i);
}
```



##### 遍历容器（使用迭代器iterators）

```
Qt的容器类提供了两种类型的迭代器：Java风格迭代器和STL风格迭代器
如果只是想按顺序遍历一个容器中的项目，那么还可以使用Qt的foreach关键字
```

Java风格迭代器

```
java风格迭代器从Qt4时被引入，使用上比STL风格迭代器要方便很多，但是在性能上稍微弱于后者。每一个容器类都有两个Java风格迭代器数据类型：一个提供只读访问，一个提供读/写访问
```



![java_iterator](C:\Users\Gaopeng\Pictures\Saved Pictures\java_iterator.png)

![QListIterator常用API](C:\Users\Gaopeng\Pictures\Saved Pictures\QListIterator常用API.png)

###### JAVA风格迭代器

QList为例

```c++
#include <QList>
#include <QListIterator>
#include <QMutableListIterator>

QList<QString> list;
list << "A" << "B" << "C" << "D";

QListIterator<QString> i(list);

qDebug() << "the forward is: ";
while (i.hasNext()) {
    qDebug() << i.next();
}

qDebug() << "the backward is: ";
while (i.hasPrevious()) {
    qDebug() << i.previous();
}

QMutableListIterator<QString> j(list);
j.toBack();
while (j.hasPrevious()) {
    if(j.previous() == "B")
        j.remove();
}
j.insert("Q");
j.toBack();
if(j.hasPrevious())
    j.previous() = "N";
j.previous();
j.setValue("M");
j.toFront();
qDebug() << "the forward is: ";
while (j.hasNext()) {
    qDebug() << j.next();
}
```



QMap为例

```c++
#include <QMap>
#include <QapIterator>
#include <QMutableMapIterator>

QMap<QString,QString> map;
map.insert("Paris","France");
map.insert("Guatemala City","Gutemala");
map.insert("Mexico City","Mexico");
map.insert("Moscow","Russia");

QMapIterator<QString,QString> i(map);
while (i.hasNext()) {
    i.next();
    qDebug() << i.key() << ":" << i.value();
}
if(i.findPrevious("Mexico"))
    qDebug() << "find Mexico";

QMutableMapIterator<QString,QString> j(map);
while (j.hasNext()) {
    if(j.next.key.endsWith("City"))
        j.remove();
}
while (j.hasPrevious()) {
    j.previous();
    qDebug() << j.key() << ":" << j.value();
}
```



###### STL风格迭代器

```
STL风格迭代器兼容Qt和STL的通用算法（generic algorithms）,而且在速度上上进行了优化。每一个容器类都有两个STL风格迭代器类型；一个提供了只读访问，另一个提供了读/写访问，因为只读迭代器比读/写迭代器要快很多，所以应尽可能使用只读迭代器
```

![stl_iterator](C:\Users\Gaopeng\Pictures\Saved Pictures\stl_iterator.png)

![stl_Iteratorpos](C:\Users\Gaopeng\Pictures\Saved Pictures\stl_Iteratorpos.png)

![](C:\Users\Gaopeng\Pictures\Saved Pictures\stl_iteratorAPI.png)

Example

```c++
#include <QList>
#include <QMap>
#include <QDebug>

QList<QString> list;
list << "A" << "B" << "C" << "D";

QList<QString>::iterator i;
qDebug() << "the forward is: ";
for (i = list.begin(); i != list.end(); i++) {
    *i = *i.toLower();
    qDebug() << *i;
}

qDebug() << "the backward is: ";
while (i != list.begin()) {
    --i;
    qDebug() << *i;
}

QList<QString>::const_iterator j;
for (j = list.constBegin(); j != list.constEnd(); j++) {
    qDebug() << *j;
}

QMap<QString,int> map;
map.insert("one",1);
map.insert("two",2);
map.insert("three",3);

QMap<QString,int>::const_iterator p;
qDebug() << "the forward is: ";
for(p = map.constBegin(); p != map.constEnd() ; p++) {
    qDebug() << p.key() << ":" << p.value();
}
```

###### foreach关键字

```
foreach关键字是Qt向C++语言中添加的一个用来进行容器顺序遍历的关键字，它使用预处理器来进行实施。
在foreach循环中也可以使用break和continue语句。可以看到，使用foreach()关键字进行容器的遍历非常便捷；当不愿意使用迭代器时，就可以使用foreach来代替。
```

Example

```c++
#include <QList>
#include <QMap>
#include <QMultiMap>

QList<QString> list;
list.insert(0,"A");
list.insert(1,"B");
list.insert(2,"C");
qDebug() << "the list is :";
foreach (QString str, list) {
    qDebug() << str;
}

QMap<QString,int> map;
map.insert("first",1);
map.insert("second",2);
map.insert("third",3);
qDebug() << endl << "the map is :";
foreach (QString str, map.keys()) {
    qDebug() << str << ":" << map.value(str);
}

QMultiMap<QString,int> map2;
map2.insert("first",1);
map2.insert("first",2);
map2.insert("first",3);
map2.insert("second",2);
qDebug() << endl << "the map2 is :";
QList<QString> keys = map2.uniqueKeys();
foreach(QString str,keys) {
    foreach(int i,map2.value(str))
        qDebug() << str << ":" << i;
}
```

#### 通用算法algorithm

```c++
//将list所有项目复制到vec中	//参数：原容器首，原容器尾，新容器首	返回值:QString
std::copy算法:	std::copy(list.begin(),list.end(),vec.begin()) 

//从list开始到结束所有项目与vec开始到结束等数量比较 //参数：原容器首，原容器尾，新容器首  返回值:bool
std::equal算法：   std::equal(list.begin(),list.end(),vec.begin()) 

//从list中查找"two",返回第一个对应的值的迭代器，如果没有找到则返回end()	返回值:QList<QStirng>
std::find算法：    QList<QString>::iterator i = std::find(list.begin(),list.end(),"two") 

//为list容器中填充元素，参数：原容器首 原容器尾 要填充的元素	返回值 void
std::fill算法:	std::fill(list.begin(),list.end(),"eleven");

//查找容器中某个元素的个数	参数：原容器首 原容器尾 被查找元素的名称 返回值int
std::count算法：	std::count(list.begin(),list.end(),6); //查找容器中6的个数

//返回容器中某个元素出现的位置  返回值QList<int>
std::lower_bound算法: QList<int>::iterator j = std::lower_bound(list.begin(),list.end(),5);

//使用快速排序算法对list2进行升序排序，排序后两个12的位置不确定 参数 容器首 容器尾 返回值 void
std::sort算法:	QList<int> list; list << 1 << 3 << 5 << 2 << 6; std::sort(list.begin(),list.end());

//使用一种稳定排序算法对list2进行升序排序，
std::stable_sort算法:std::stable_sort(list.begin(),list.end());

//在qSort()算法中使其反向排序 qSort(list.begin(),list.end(),std::greater<int>()) 
std::greater算法:qSort(list.begin(),list.end(),std::greater<int>());

//交换算法	std::swap(a,b)
std::swap算法:	double pi = 3.14; double e = 2.17; std::swap(pi,e);	qDebug() << pi << e;
```

#### √牛逼的正则表达式（regular expression）

定义：就是在一个文本中匹配子字符串的一种模式(pattern)，它可以简写为regexp。

一个regexp主要应用在以下几个方面:

验证：regexp可以测试一个子字符串是否符合一些规范。例如：是否是一个整数或者不包含任何空格等

搜索：regexp提供了比简单的子字符串匹配更强大的模式匹配。例如：匹配单词mail或者letter，而不匹配单词email、mailman或者letterbox

查找和替换: regexp可以使用一个不同的字符串替换所有匹配的子字符串，例如，使用Mail来替换一个字符串中所有的M字符，但是M字符后面有ail时则不进行替换

字符串分割：regexp可以识别在哪里进行字符串分割。例如，分割制表符隔离的字符串

Regexps由表达式（expressions）、量词（quantifiers）和断言（assertions）组成。

最简单的表达式就是一个字符，比如x和5

## 六、高级编码风格

##### 1.善用全局宏定义#define

```c
#define TIMES QDateTime::currentDateTime().toString("yyyy-MM-dd hh:mm:ss")
#define APPPATH QCoreApplication::applicationDirPath()
```

##### 2.明确注意编码格式QTextCodec

```c
#pragma execution_character_set("utf-8")

#ifdef (QT_VERSION <= QT_VERSION_CHECK(5,0,0))
#ifdef _MSC_VER
	QTextCodec *codec = QTextCodec::codeForName("gbk");
#else
    QTextCodec *codec = QTextCodec::codeForName("utf-8");
#endif
    QTextCodec::setCodecForLocale(codec);
	QTextCodec::setCodecForCStrings(codec);
     QTextCodec::setCodecForTr(codec);
#else
    QTextCodec *codec = QTextCodec::codecForName("utf-8");
    QTextCodec::setCodecForLocale(codec);
#endif
```

##### 3.if,for,while编码风格

```c
//if风格
if () {
	xxx;
} else if () {
	xxx;
} else {
	xxx;
}

//for风格
for (int i = 0; i < 100; i++) {
    xxx;
}

//while风格
while () {
    xxx;
}
```

##### 4.类的成员函数如果不改变成员变量，建议加const

```c++
class A
{
public:
	void getValue(int value) const 
    {
        return m_value;
    }
private:
    int m_value;
}
```

##### 5.简单的槽操作可用Lambda表达式

```c++
QPushButton *btn = new QPushButton(this);
connect(brn,&PushButton::clicked,[=](){
	qDebug() << QObject::tr("你好,Qt");
}); //切记此处信号槽的发送信号不要使用SIGNAL()
```

##### 6.格式转换要习惯用与static_cast<T>exp,将exp转换成T类型

``` c
//使用说明 static_cast<T> (exp)，	T的类型和被赋值的新变量类型保持一致
char a = c;
int b = static_cast<int> (a);
double c = static_cast<double> (a);
qDebug() << "a = " << a << endl;
qDebug() << "b = " << b << endl;
qDebug() << "c = " << QString::number(c,'f',2) << endl;
```

##### 7.命名规范

###### 规范1(数据类型)

```c++
变量命名规则：
一.用最短字符表示最准确的意义。
二.使用变量前缀。
1.整型前缀
　　int nId; 　　 　　     　　 //int前缀：n
　　short sId; 　　    　　　　//short前缀：s
　　unsigned int unId 　　　  // unsigned int 前缀：un
　　long lId; 　　　　　　　　 //long前缀：l　　

2.浮点型前缀
　　float fValue;　　　　　　 //float前缀：f
　　double dValue; 　　　　  //double前缀：d

3.字符型前缀
　　char chChar;　　　　　　//char前缀：ch

4.字符串前缀
　　char szPath; 　　　　　  //char字符串前缀：sz
　　string strPath; 　　　　  //string字符串前缀：str
　　CString strPath; 　　　  //MFC CString类前缀：str

5.布尔型前缀
　　bool bIsOK; 　　　　 　  //bool类型前缀：b
　　BOOL bIsOK; 　　　　    //MFC BOOL前缀：b

6、 指针型前缀
　　char* pPath; 　　 　　  //指针前缀：p

7.数组前缀
　　int arrnNum[]; 　　　　   //数组前缀：arr
　　CString arrstrName[]; 　 //数组前缀+类型前缀+名称

8.结构体前缀
　　STUDENT tXiaoZhang;   //结构体前缀：t

9.枚举前缀
　　enum emWeek; 　　      //枚举前缀：em

10.字节的前缀
　　BYTE byIP; 　　　　　　 //字节前缀：by

11.字的前缀
　　DWORD dwMsgID; 　　  //双字前缀：dw
　　WORD wMsgID; 　　     //单字前缀：w

12.字符指针前缀
　　LPCTSTR ptszName;     //TCHAR类型为ptsz
　　LPCSTR pszName;        //pcsz
　　LPSTR pszName; 　　   //psz

13.STL容器前缀
　　vector vecValue; 　　  //vector容器前缀：vec

14.RECT矩形结构前缀
　　RECT rcChild; 　　　　 //rc
　　CRECT rcChild; 　　　  //rc

15.句柄前缀
　　HWND hWndDlg; 　　   //h
　　HBRUSH hBr; 　　　　  //h
　　HPEN hPen; 　　　　   //h
　　HBITMAP hBmpBack;   //h

16.Windows颜色前缀
　　COLORREF crFont;     //cr

17.Windows DC前缀
　　CDC dcClient; 　　　  //dc

18.STL
　　说明：vec表示vector容器的前缀，为了简化变量，变量体后面不再使用前缀
　　vector<int> vecValue;
　　list<double> lstInfo;

三.类的成员变量以m_开头，后面为变量，变量同时还要加前缀。
　　CString m_strName;    //m_开头+类型前缀+名称

四.定义一个变量，为了简化，在不影响变量意义的情况下，可仅仅使用前缀。
　　RECT  rc;

五.全局变量一律以g_开头，后面为变量，变量同时还要加前缀。
　　int g_ID;                  //g

六.定义结构体，保证C和C++兼容，采用typedef语句，并且结构体类型全部大写，以T_开头，指针形式以PT_开头。
　　typedef struct tag TSTUDENT
　　{
　　　　int nId;
　　　　CString strName;
　　}STUDENT, *PSTUDENT;
　　STUDENT tXiaoZhang;  　　　　//完整定义结构体

七.变量由多个单词组成，则每个单词的首个字母大写。
　　int nStudentID;
　　CString strStudentName;

八.定义一个类以C或者T做为类名前缀。
　　class CMyListCtrl;
　　class TMyListCtrl;

九.MFC控件绑定值类别或者控件类类别，需要以m_开头并且加前缀。
　　CEdit m_EDT_strValue; 　　　　//Edit绑定控件类别
　　CListBox m_LB_nName; 　　　  //ListBox
　　CListCtrl m_LC_Name; 　　　　 //ListCtrl;
　　CComboBox m_CB_Name; 　　  //ComboBox

十.控件ID尽量简化并表明控件类型和意义。
　　Button IDC_BNT_NAME;
　　Edit IDC_EDT_NAME;
　　ListBox IDC_LB_NAME;
　　ListCtrl IDC_LC_NAME;
　　ComboBox IDC_CB_NAME;
```

###### 规范2(数据类型)

```c
★匈牙利命名法：基本原则是：变量名＝属性＋类型＋对象描述，其中每一对象的名称都要求有明确含义，可以取对象名字全称或名字的一部分。命名要基于容易记忆容易理解的原则。保证名字的连贯性是非常重要的。
Camel命名法：即骆驼式命名法，原因是采用该命名法的名称看起来就像骆驼的驼峰一样高低起伏。
Camel命名法有两种形式：混合使用大小写字母和单词之间加下划线，例如runFast和run_fast都属于Camel命名法。
Pascal命名法：与Camel命名法类似，不过Pascal命名法的首字母为大写字母。

★1、在所有命名中，都应使用标准的英文单词或缩写。不得使用拼音或拼音缩写，除非该名字描述的是中文特有的内容，如半角、全角, 声母、韵母等。
★2、所有命名都应遵循望文知义原则，即名称应含义清晰、明确。
★3、所有命名都不易过长，应控制在规定的最大长度以内。
★4、所有命名都应尽量使用全称。
5、如果命名使用缩写，则应该使用《通用缩写表》（见附录）中的缩写；原则上不推荐使用《通用缩写表》以外的缩写，如果使用，则必须对其进行注释和说明。

1、工程名：不强制统一。
2、文件名：
基于工程名，开头3个字母应表明与哪一个工程相关。
后面的字母应能够区别不同的功能。
不区分大小写。
长度不限于8.3格式，建议不多于30个字符。
若文件用于定义和实现类，建议文件名与类名保持一致。
3、函数名：
参照 Windows API 的命名规范。
推荐使用动宾结构。函数名应清晰反映函数的功能、用途。
函数名最长不得超过30个字符。
★函数名第一个字母必须大写。
★全局函数必须以小写前缀"g"开头。
4、变量名：
★原则上，变量名的命名遵从匈牙利记法。即：前缀 + 类型 + 变量名
1）格式：
[m_|s_|g_] type [class name|struct name] variable name
2）解释：
★m_ ： 类的成员变量
★ms_：类的静态成员变量
★s_ ：静态全局变量
★g_ ：普通全局变量
类型缩写（type）
★char, TCHAR： ch
★char[]，TCHAR[]： sz
★string： str
★bool, BOOL： b
★int, __int16,__int32,__int64： n
★long： l
★double： d
★float： f
★BYTE： by
★WORD： w
★DWORD： dw
★unsigned： u
★function： fn
★p ：pointer
★lp ：long pointer
变量名最长不得超过20个字符。

5、类名：
★必须以大写"C"开头，后面字母反映具体含义，以清晰表达类的用途和功能为原则。
★接口必须以大写"I"开头，代表 Interface 。
★当名称由多个单词构成时，每一个单词的第一个字母必须大写。
★6、结构体名、宏名、枚举名、联合名：
★全部大写。
★枚举名加小写前缀"enum"。
例：
typedef enum _CFILE_OPEN_MODE
{
enumOPEN_READONLY = 0,
enumOPEN_READWRITE = 1,
enumCREATE_ALWAY = 3
 } CFILE_OPEN_MODE;

//·宏名加小写前缀"def"。
例：#define defMAXNUMBER 100
结构名加小写前缀"tag"，之后必须以大写"C"开头。
例：
typedef struct tagKPOINT
{
int x;
int y;
} KPOINT;

//·联合名加小写前缀"uni"。
例：

typedef union _VARIANT{
char unichVal;
int uninVal;
long unilVal;
float uniftVal;
...
} VARIANT;



在.h/.cpp的开头应有一段格式统一的说明，内容包括：
a. 文件名 (FileName)；
b. 简短说明文件功能、用途 (Comment)；
c. 创建人 (Creater)；
d. 文件创建时间 (Date)。
例：

/*!
  *@file
  *@brief
  *@author
  *@date
  */
除非极其简单，否则对函数应有注释说明。内容包括：功能、入口/出口参数，必要时还可有备注或补充说明。
每行代码的长度推荐为80列，最长不得超过120列；折行以对齐为准。
例：

HANDLE CSOpenFile(const char cszFileName[],<br>int nMode);
或者：
BOOL CSReadFile(<br>HANDLE hFile,<br>void *pvBuffer,<br>int nReadSize,<br> int *pnReadSize<br>);<br>
循环、分支代码，判断条件与执行代码不得在同一行上。
例：正确：

if (n == -2)
    n = 1;
else
    n = 2;
不得写做：

if (n == -2) n = 1;
else n = 2;
指针的定义，* 号既可以紧接类型，也可以在变量名之前。
例：可写做：

int* pnsize;
也可写做：

int *pnsize;
但不得写做：

int * pnsize;
在类的成员函数内调用非成员函数时，在非成员函数名前必须加上“::”。
函数入口参数有缺省值时，应注释说明。
例:

BOOL KSSaveToFile(const char cszFileName[],BOOL bCanReplace /* = TRUE */);
或者：

BOOL KSSaveToFile(const char cszFileName[],BOOL bCanReplace // = TRUE );
else if 必须写在一行。
与‘{’、‘}’有关的各项规定：
9.1‘{’、‘}’应独占一行。在该行内可有注释。
例：正确：

for (i = 0; i < cbLine; i++)
{ // .....
    printf("Line %d:", i);
    printf("%s\n", pFileLines);
}
不得写做：

for (i = 0; i < cb; i++)
{printf("Line %d:", i);<br>printf("%s\n", pFileLines);}
9.2‘{’必须另起一行，‘{’之后的代码必须缩进一个Tab。‘{’与‘}’必须在同一列上。
例：正确：

if (i > 0)
{<br>　　m = 1;<br>　　n++;
}
不得写做：

if (i > 0) {
m = 1;
n++;
}
例外：

if (i == 0)
{ ASSERT(FALSE); return; }
9.3 在循环、分支之后若只有一行代码，虽然可省略‘{’、‘}’，但不推荐这么做。若省略后可能引起歧义，则必须加上‘{’、‘}’。
与空格有关的各项规定。
10.1 在所有两目、三目运算符的两边都必须有空格。在单目运算符两端不必空格。但在‘->’、‘::’、‘.’、‘[’、‘]’等运算符前后，及‘&’（取地址）、‘*’（取值）等运算符之后不得有空格。
例：正确：

int n = 0, nTemp;
for (int i = nMinLine; i <= nMaxLine; i++)
不得写做：

int n=0, nTemp;
for ( int i=nMinLine; i<=nMaxLine; i++ )
10.2 for、while、if 等关键词之后应有1个空格，再接‘(’，之后无空格；在结尾的‘)’前不得有空格。
例：正确：

if (-2 == n)
不得写做：

if(-2 == n)
或

if ( -2 == n )
10.3 调用函数、宏时，‘(’、‘)’前后不得有空格。
例：正确：

printf("%d\n", nIndex);
不得写做：

printf ("%d\n", nIndex);

printf( "%d\n", nIndex );
10.4 类型强制转换时，‘(’‘)’前后不得有空格
例：可写做：

(KSFile*)pFile;
也可写做：

(KSFile *)pFile
不得写做：

( KSFile* )pFile

( KSFile * ) pFile
与缩进有关的各项规定
11.1 缩进以 Tab 为单位。1 个 Tab 为 4 个空格
11.2 下列情况，代码缩进一个 Tab:
函数体相对函数名及‘{’、‘}’。
例：

int Power(int x)
{
　　return (x * x);
}
if、else、for、while、do 等之后的代码。
一行之内写不下，折行之后的代码，应在合理的位置进行折行。若有 + - * / 等运算符，则运算符应在上一行末尾，而不应在下一行的行首。
11.3 下列情况，不必缩进：switch 之后的 case、default。
例：


switch (nID)
{
case ID_PLAY:
　　......
　　break;
case ID_STOP:
　　......
　　break;
default:
　　......
　　break;
} 

```

###### 规范3(组件名称)

```c++
/*组件名称			简写				示例
**QPushButton		btn
**QRadioButton		rBtn
**QToolButton		tBtn
**QLabel		    lbl
**QWidget			wgt
**QLineEdit			lineEdit
**QTextEdit			txtEdit
**QTextBrowser		txtBwr
**QTabWidget		tabWgt
**QTableWidget		tableWgt
**QTableView		tableVw
**QStackedWidget	stackWgt
**QCheckBox			chkBox
**QComboBox			cmoBox
**QGroupBox			gopBox
**QListWidget		listWgt
**QListView			listVw
**QTreeWidget		treeWgt
**QTreeView			treeVw
**QSpinBox			spinBox
**QDoubleSpinBox	 doubleSpinBox
**QDateEdit			dateEdit
**QTimeEdit			timeEdit
**QDateTimeEdit		datetimeEdit
**QProgressBar		progressBar		progressBar1
**QAction			act				actCut	actCopy		
**QMenuBar 			menuBar				
**QMenu				menu			menu	menu_1	menu_2
**QToolBar			ToolBar			mainToolBar
**QStatusBar		statusBar		
**QFontComboBox		fontComboBox
*/
```

##### 8.if(exp) 和 if(!exp)

```c
if (exp) {						 //判返回值的方法，exp != 0
    qDebug() << "exp != 0";	  	   //exp为真时对应的表达式
} else if (!exp) {				 //判返回值的方法，exp == 0
    qDebug() << "exp == 0";	      //exp为假时对应的表达式
}
```

##### 9.按钮样式设置参考

```c++
Example1:  	
	ui->pushButton_FileOpt->setFlat(true);	//设置按钮边框是否去掉
    ui->pushButton_FileOpt->setStyleSheet("QPushButton{background: transparent;}"); //透明
    ui->pushButton_FileOpt->setToolTip("文件选择"); //小提示，鼠标放在上面，会提示此信息
    ui->pushButton_FileOpt->setIcon(QIcon("res/open.png")); //按钮图片

Example2:
	this->setStyleSheet("background-color:rgb(204,229,255);color:rgb(255,0,0);font:12pt 宋体");
```

##### 10.获取文件的内容大小

fseek(pfile,0,SEEK_END);

int nFileSize = ftell(pfile);

fseek(pfile,0,SEEK_SET)l

```c++
Example:
    FILE* pfile = NULL;
    pfile = fopen(strGDProcess.toLocal8Bit().constData(),"rb");
    if(NULL == pfile)
    {
        IGetCommu()->SendInfo(log_type_error, L"读取惯导流程文件失败");
        return -1;
    }
    fseek(pfile, 0, SEEK_END);
    int nFileSize = ftell(pfile);
    fseek(pfile, 0, SEEK_SET);
    int nCmdCount = nFileSize / sizeof(stRDGDFlowFileData);
    stRDGDFlowFileData *pCmdBuf = new stRDGDFlowFileData[nCmdCount];
    memset(pCmdBuf,0,sizeof(stRDGDFlowFileData)*nCmdCount);

    if(nCmdCount != fread(pCmdBuf, sizeof(stRDGDFlowFileData), nCmdCount, pfile))
    {
        fclose(pfile);
        pfile = NULL;
        IGetCommu()->SendInfo(log_type_error, L"流程文件长度错误");
        return -1;
    }
    fclose(pfile);
    pfile = NULL;
```

##### 11.大小端BE/LE（important）

```
大端模式：Big-Endian		  低字节存储在高地址位，高字节存储在低地址位
小端模式: Little-Endian	   低字节存储在低地址位，高字节存储在高地址位
举例0x2345		地址高低位：从左往右，地址位逐渐降低		字节高低位：从左往右，字节位逐渐升高
大端模式：0x23 0x45		
小端模式: 0x45 0x23
```

##### 12.QtCreator中生成C语言的黑色控制台

```c++
//在pro中文件中加入CONFIG += console
#include <QtWidgets>

int main(int argc,char *argv[])
{
    QString s;
    QTextStream in(stdin,QIODevice::ReadOnly);
    in.setCodec("GB18030");
    in >> s;	//把控制台输入的内容赋值给s
    QTextStream out(stdout,QIODevice::WriteOnly);
    out << s;
}
```

##### 13.通过QTextStream读取文本文件

```c++
#include <QtWidgets>

int main(int argc,char *argv[])
{
    QFile f("F:/1.txt");
    f.open(QIODevice::ReadOnly);
    QTextStream in(&f);
    in.setCodec("GB18030");
    QChar c;

    //逐字读取
    in >> c;
    qDebug() << c << endl;
    in >> c;
    qDebug() << c << endl;

    //一个单词接一个单词读取
    in.seek(0);
    QString s;
    in >> s;
    qDebug() << s << endl;
    in >> s;
    qDebug() << s << endl;

    //读取指定个数的字符
    in.skipWhiteSpace();
    s = in.read(10);
    qDebug() << s << endl;

    //逐行读取
    s = in.readLine();
    qDebug() << s << endl;

    //读取整个文本
    in.seek(0);
    s = in.readAll();
    qDebug() << s << endl;

    in.seek(0);
    //使用for循环读取
    while (!in.atEnd())
    {
        s += in.readLine();
        qDebug() << s << endl;
    }
}

```



## 七、常见问题

##### 1.BesNew使用问题

```c++
问题：点击bes.exe,报告错误信息：Failed to set data for ''
解答：使用管理员权限打开bes.exe就可以了
```

##### 2.启动程序失败，路径或者权限错误？

```tex
情况1：当代码生成的程序一直是带着管理员权限的标志
	将QtCreator软件采用管理员权限打开再使用
情况2：检查项目路径中是否包含了中文路径或非法路径导致无法生成exe或dll
情况3：如果手动将生成的exe设置为管理员权限了，那么请将生成的exe设置回普通权限
```

##### 3.类的定义必须带分号，类里的成员函数结尾可以不加分号

```c++
class A : public QObject
{
	void func()	//此处可以不加;
	int num;
}; //此处必须加;
```

##### 4.回车换行（"\r\n"）

```
\r:回到当前行的行首，而不会换到下一行，如果接着输入的话，本行的内容会被逐一覆盖
\n：换行，换到当前位置的下一行，而不会回到行首
```

##### 5.memcpy()将参数给到数组的某个位置

```c++
typedef struct st_pub
{
	int a;
	quint8 arr[66];
}stpub;

stpub m_pub;

memset(&m_pub,0,sizeof(m_pub));

quint16 n1 = 66;
quint16 n2 = 88;

memcpy(m_pub.arr,&n1,sizeof(n1));
memcpy(m_pub.arr+2,&n2,sizeof(n2));

```





## 八、HWA学习

### 1.1553流程（参考代码：38s_lp_zj_	应用场地：38所）

```c++
//流程控制分为2大模块，选择流程文件和运行流程文件
//选择流程文件代码:
	QString downloadFilePath = "";
	downloadFilePath = QFileDialog::getOpenFileName(this,tr("Open Data File"),
                                                    "../../bin/debug/Data/1553ProcessFile",
                                                    tr("Data File(*.dat) ;; All File(*)"));
	if ("" == downloadFilePath)
        return;
	strFlowFile = downloadFilePath;	//QString strFlowFile;(声明于头文件类的成员下，作为类的成员变量使用，方便多次使用)
	QFileInfo info(strFlowFile);
	ui->lineEdit_processFileName->setText(info.fileName()); //将文件名显示到对应的编辑输入栏中
	ui->lineEdit_processFilePath->setText(info.path()); //将文件路径显示到对应的编辑输入栏中
	emit sig_addInfoIntem("流程文件:" + strFlowFile + "选择完成");
	//对应的槽函数(信息栏中显示，示例：[18:18:18]流程文件：F:/bin/debug/Data/1553ProcessFile/flowTestFile.dat)选择完成
            void ControlProcess::slot_addInfoIntem(QString info)
            {
                QString time = QTime::currentTime().toString("hh:mm:ss");
                ui->listWidget->addItem("["+time+"]  "+info);
                ui->listWidget->setCurrentRow(ui->listWidget->count()-1);
            }
/*综上所述，关于选择流程文件部分总结以下几点
**1.通过QFileDialog::getOpenFileName()创建文件对话框，选择我们想要执行的流程文件，将其保存在流程文件临时变量1中
**2.将临时变量1中的数据赋给类下的流程文件(变量2)中
**3.获取点1选中的流程文件信息，并把流程文件的名称和路径显示到界面指定的位置
**4.选择流程文件这个大操作执行完毕后，通过信息窗口listWidget显示出来，告诉我们在什么时候选择的哪个流程文件完成了。
*/

//运行流程文件代码:
	QString strName;
	strName = ui->pushButton_StartRun->text(); //获取流程按钮的名称(流程开始/流程停止)
	if ("流程开始" == strName)
    {
        str1553Process = strFlowFile; //将类下的流程文件(变量2)赋给类下的1553流程(变量3)
        if ("" == str1553Process)
        {
            IGetCommu()->SendInfo(log_type_error,L"请选择相应的流程文件");
            return;
        }
        if (IGetDev()->getRunningState())
        {
            QMessageBox::warning(NULL,"提示","请将回波回放停止再开始流程",
                                 QMessageBox::Yes|QMessageBox::No,QMessageBox::Yes);
            return;
        }
        ui->pushButton_StartRun->setIcon(QIcon("res/stop0.png")); //设置流程启动按钮图标
        ui->pushButton_StartRun->setText("流程停止"); //设置流程启动按钮新名称
        ui->pushButton_StartRun->setIconSize(QSize(32,32)); //设置图标大小
        bRunFlowFlag = false; //运行流程标志  std::atomic_bool  bRunFlowFlag;
        m_StrorageBoard.SetOperRegPara(0xF,1); //存储板复位
        m_StrorageBoard.SetRegValue(0x424,1); //回放,给424写1，这是要干啥？			  xxxxxx??????
        IGetDev()->ResetInterCard(0); //接口板复位
        IGetDev()->ResetMIdFrqCard(0); //中频板复位
        m_StrorageBoard.SetOperRegPara(0x150,65536); //stata盘一次性写入长度 			xxxxxxx??????
        SetFlowMidFrqPara(); 	 //中频参数配置         	子函数			
        IGetDev()->setRfParam(); //射频参数配置     		子函数
        //配置文件中读数据
        quint32 uValue = 0;
      	QString strCfgFilePath;
        strCfgFilePath = m_currPath + "/config/config.ini";
        QSettings ini(strCfgFilePath,QSettings::IniFormat);
        ini.setIniCodec("GBK");
        uValue = objIni.value("/1553BOpt/1553Opt").toUInt(); //0:4M			1:1M
        IGetDev()->WtriteReg(0,0x2E0,uValue,INTREFACEBOARD,0);  //1553B 4M,将4M的1553B写入到接口板寄存器0x2E0中
        emit sig_SetRecordInfo(1); //记录回波
        if (ui->pushButton_UdpStartStop->text() != "UdpStop")
        {
            bRunEchoUdpRevcieFlag = true;
            std::thread thReviceNetEchoWave{&ControlProcess::slot_m_RecNetEchoData,this};
            thReviceNetEchoWave.detach();
        }
        StartRunProcess(); //开始运行流程				子函数
        StartGetFlowMode(); //开始获取流程模式		   子函数
    }
	else
    {
        bRunFlowFlag = true; //运行流程标志
    }
/*综上所述，关于运行流程文件部分总结以下几点
**判断流程开始按钮的名称
	流程开始：
		1.(关键)将类下的流程文件(变量2)赋给类下的1553流程(变量3)
		2.获取流程运行的状态，如果当前正在回放回波，报错退出
		3.设置流程开始按钮的样式，改为停止样式
		4.运行流程标志设置为false，代表当前正在执行流程过程中
		5.接口板，存储板，中频板三类板卡复位
		6.配置中频参数和射频参数
		7.将1553B的4M写入到接口板的寄存器2E0中
		8.开始记录回波
		9.(核心)开始运行流程
		10.开始获取流程模式
	流程停止：
		运行流程标志设置为true，代表流程已停止
*/

//子函数：开始运行流程
void ControlProcess::StartRunProcess()
{
	CloseThread(m_thRunProcess);
	m_thRunProcess.start(); //开始运行流程		孙子函数
	IGetCommu()->SendInfo(log_type_info, L"流程开始...");
}

//孙子函数：
void ControlProcess::slot_StartRunProcess()
{
	qint32 iret = -1; //充当大多数函数返回值，判断函数执行情况
	quint32 uRegValue = 0;
	qint32 iFlowNum = 0;
    
	iret = Get1553File(iFlowNum); //获取1553文件，iFlowNum:流程数目(关键)
	if (iret < 0)
	{
        bRunFlowFlag = true; //运行流程标志设置为true,代表流程退出，结束了！！！
	}
    quint32 lastIndex{0}; //上一次的流程条目
    emit sig_showProcessProgress(0,iFlowNum);
}
```



## 九、C++基础学习

### 1.在main()执行前和执行后的代码可能是什么？

main()函数执行之前，**主要就是初始化系统相关资源**。

### 2.在创建xxx.ui设计师界面文件时，构造后会生成一个ui_xxx.h文件

比如创建了一个form.ui的xml文件，构造后会生成一个ui_form.h的c++头文件

## 十、Gitbash

### 1、gitbash常用命令

```bash
git init 初始化 git，只有初始化了以后才可以使用 git 相关命令。
git clone 获取远程项目，并下载到本地。远程库的地址在 GITHUB 项目中会有提供。
git status 查看本地修改与服务器的差异。
git add . 将这些差异文件添加，这样就可以提交了。
git commit –m “这里是注释” 提交更改到服务器。
git checkout master 更改到master库。
git pull 将服务器最新的更改获取到本地。
git merge local master 将本地的local合并到远程的master上。
git push origin master 正式提交到远程的master服务器上。
还有“git tag”，“git diff”，“git show”，“git log”，“git remote”等。
```

