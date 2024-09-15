函数注释例子：

	/**
	 * @brief 一键换装备-搜索装备
	 * @param pid 窗口id
	 * @param name 要换的装备名
	 * @return 无
	 */
	void Searchbag(HWND pid,QString name){
	    dm.MoveTo(736,382);
	    dm.LeftClick();
	    QString s=name;
	    foreach(QChar c, s)
	        PostMessage(pid, WM_CHAR, c.unicode(), 0);
	    Delay(500);
	    dm.MoveTo(797,380);
	    dm.LeftClick();
	}


源码使用方法
--------

* source文件夹内全部文件下载下来，在**qt creater**中打开**untitled.pro**
* 在项目中，构建设置中设置编译套件为**Qt-5.9.0-MinGW-32**，也就是qt最原始的编译套件，不是MSVC什么的
* 编译无问题后，在程序的release或者debug目录中**（取决于你选择的模式）**，文件结构应与图中一样，否则程序会自动结束**（检查缺少的文件/文件夹，在logonseer文件夹中都有）**

		├─bearer
		├─font
		├─gif
		├─iconengines
		├─imageformats
		├─json
		├─pic
		├─platforms
		├─seer背包
		├─translations
		└─工具
		    ├─dm
		    ├─Fiddler
		    │  ├─FiddlerHook
		    │  │  ├─Content
		    │  │  ├─defaults
		    │  │  │  └─preferences
		    │  │  ├─locale
		    │  │  │  └─en-US
		    │  │  └─skin
		    │  ├─ImportExport
		    │  ├─Inspectors
		    │  ├─ResponseTemplates
		    │  ├─Scripts
		    │  ├─Tools
		    │  ├─检查
		    │  └─汉化截图
		    └─赛尔数据计算器
		        ├─帮助文件
		        │  ├─Bin
		        │  └─Easter Eggs
		        ├─数据文件
		        │  ├─刻印
		        │  ├─套装
		        │  │  └─目镜
		        │  ├─属性
		        │  ├─种族值
		        │  ├─称号
		        │  ├─设置
		        │  └─魂印特训
		        ├─记录文件
		        │  ├─属性表格
		        │  └─精灵培养
		        └─资源文件


