#
# Makefile for miscellaneous I2C chip drivers.
#
# Do not add new drivers to this directory! It is DEPRECATED.
#
# Device drivers are better grouped according to the functionality they
# implement rather than to the bus they are connected to. In particular:
# * Hardware monitoring chip drivers go to drivers/hwmon
# * RTC chip drivers go to drivers/rtc
# * I/O expander drivers go to drivers/gpio
#
# FEATURE_M7LAB

#obj-$(CONFIG_SENSORS_MT9T013)	+= mt9t013.o
obj-$(CONFIG_SENSORS_MMC328X)	+= mmc328x.o
obj-$(CONFIG_ECOMPASS)		+= mecs.o
obj-$(CONFIG_BOSCH_BMA222)	+= bma222_driver.o bma222.o 
obj-$(CONFIG_SENSORS_TAOS)	+= taos.o

ifeq ($(CONFIG_I2C_DEBUG_CHIP),y)
EXTRA_CFLAGS += -DDEBUG
endif

ifeq ($(CONFIG_BOSCH_BMA222_USE_SMBUS),y)
EXTRA_CFLAGS += -DBMA222_SMBUS
endif
#ifeq ($(CONFIG_BOSCH_BMA222_WITH_DEBUG),y)
#EXTRA_CFLAGS += -DBMA222_DEBUG
#endif
ifeq ($(CONFIG_BOSCH_BMA222_HAS_EARLYSUSPEND),y)
EXTRA_CFLAGS += -DBMA222_HAS_EARLYSUSPEND
endif
