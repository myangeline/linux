# ubuntu中创建桌面快捷方式

## 1. 创建文件
这里我们只需要关注3个地方，分别为Exec=软件执行文件的路径，Icon=快捷方式图标（如果有的话），Name=快捷方式名称。根据自己软件按转的位置修改代码，保存之后关闭文件。

	[Desktop Entry]
	Categories=Development;
	Comment[zh_CN]=
	Comment=
	Exec=/home/owen/Software/eclipse/eclipse
	GenericName[zh_CN]=IDE
	GenericName=IDE
	Icon=/home/owen/Software/eclipse/icon.xpm
	MimeType=
	Name[zh_CN]=eclipse
	Name=eclipse
	Path=
	StartupNotify=true
	Terminal=false
	Type=Application
	X-DBUS-ServiceName=
	X-DBUS-StartupType=
	X-KDE-SubstituteUID=false
	X-KDE-Username=owen

## 2. 将文件名修改为eclipse.desktop

## 3. 给文件添加可执行权限
    
    $ chmod +x desktop文件 
   
或者 直接右键权限里面修改。
