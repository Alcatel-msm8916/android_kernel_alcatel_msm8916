#tct touchpanel driver

# [PLATFORM]-Add-BEGIN by TCTNB.YJ, 2014/03/25, add macro for TP driver.
ifdef CONFIG_TOUCHSCREEN_FT5X06
obj-$(CONFIG_FT5X06_TOUCHPANEL_DRIVER)	+= ft5x06_ts.o
# for focaltech tp firmware power on upgrade
	EXTRA_CFLAGS += -DFOCALTECH_PWRON_UPGRADE
	EXTRA_CFLAGS += -DFOCALTECH_TP_GESTURE
	EXTRA_CFLAGS += -DFOCALTECH_FAE_MOD
#	EXTRA_CFLAGS += -DFOCALTECH_FW_COMPAT
endif

# for Mstar msg2138A tp driver
obj-$(CONFIG_TCT_8X16_ALTO45)    += msg21xx_ts_0926.o msg21xxa_gesture.o msg21xxa_ito_test.o
	EXTRA_CFLAGS += -DMSTAR_PWRON_UPGRADE
	EXTRA_CFLAGS += -DMSTAR_ITO_TEST
	EXTRA_CFLAGS += -DMSTAR_TP_GESTURE

ifdef CONFIG_TOUCHSCREEN_GT9XX
  ifdef CONFIG_TCT_8X16_POP8LTE
obj-$(CONFIG_GT9XX_TOUCHPANEL_DRIVER)	+= gt9xx.o
#gt915 update file
obj-$(CONFIG_GT9XX_TOUCHPANEL_UPDATE)	+= gt9xx_update.o
#debug tool
obj-$(CONFIG_GT9XX_TOUCHPANEL_DEBUG)	+= goodix_tool.o
  endif
endif
# [PLATFORM]-Add-END by TCTNB.YJ

