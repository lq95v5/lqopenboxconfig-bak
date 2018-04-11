# lqopenboxconfig-bak
这是我的openbox 配置笔记
配置前先安装需要的软件

	$sudo pacman -S openbox obmenu obconf lxappearance feh tint2 compton pnmixer redshift-gtk
	$yaourt -S obmenu-generator
	
开始配置

	$mkdir -p ~/.config/openbox
	$cp /etc/xdg/openbox/{rc.xml,menu.xml,autostart,environment} ~/.config/openbox
	
使用obmenu-generator 创建右键菜单

	$obmenu-generator -s -c  -i #静态菜单
	
##openbox pulse volume  control #openbox的音量调节配置

	<keybind key="XF86AudioRaiseVolume">
	  <action name="Execute">
	    <command>pactl -- set-sink-volume 0 +5%</command>
	  </action>
	</keybind>
	<keybind key="XF86AudioLowerVolume">
	  <action name="Execute">
	    <command>pactl -- set-sink-volume 0 -5%</command>
	  </action>
	</keybind>
	<keybind key="XF86AudioMute">
	  <action name="Execute">
	    <command>pactl set-sink-mute 0 toggle</command>
	  </action>
	</keybind>


