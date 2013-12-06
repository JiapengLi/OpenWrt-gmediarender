# OpenWrt-gmediarender

Port [gmediarender-resurrect](https://github.com/hzeller/gmrender-resurrect) to OpenWrt.

## HOW TO

	cd ~
	git clone https://github.com/JiapengLi/OpenWrt-gmediarender.git
	cd openwrt/trunk
	./scripts/feeds update -a
	./scripts/feeds install -a
	cd feeds/packages
	patch -p1 < ~/OpenWrt-gmediarender/openwrt-add-gmediarender-resurrect-package.patch
	./scripts/feeds update -i
	./scripts/feeds install gmediarender
	
	make menuconfig
	// choose the right platform
	// Select gmediarender in Multimedia --> gmediarender

###Build Single Package

	make package/gmediarender/compile V=s
	make package/gmediarender/install V=s
	make package/index

	//clean and compile
	make package/gmediarender/{clean,compile} V=s

## TO DO

Test and send these patch to OpenWrt-devel. 