include $(srctree)/drivers/misc/mediatek/Makefile.custom

ccflags-y += -I$(srctree)/drivers/misc/mediatek/mach/$(MTK_PLATFORM)/$(ARCH_MTK_PROJECT)/touchpanel/ft6x06/

ccflags-y += -I$(MTK_PROJECT_PATH_ROOT)/touchpanel/ft6x06/

ccflags-y += -I$(srctree)/drivers/input/touchscreen/mediatek/
ccflags-y += -I$(srctree)/drivers/misc/mediatek/include/mt-plat/
ccflags-y += -I$(srctree)/drivers/misc/mediatek/include/mt-plat/$(MTK_PLATFORM)/include/

ifeq ($(CONFIG_MTK_PLATFORM),"mt6572")
    ccflags-y += -DMT6572
endif

ifeq ($(strip $(CONFIG_ARCH_MTK_PROJECT)),"l5460")
	ccflags-y +=	-DCONFIG_PROJECT_L5460
endif

obj-y	+=  focaltech_ctl.o
obj-y	+=  ft6x06_button.o
obj-y	+=  ft6x06_driver.o
obj-y	+=  ft6x06_iic_wrap.o
obj-y	+=  ft6x06_isp.o
obj-$(CONFIG_TP_AUTO_TEST)	+=  Test_FT5X46.o

