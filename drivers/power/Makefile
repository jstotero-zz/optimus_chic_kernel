power_supply-objs := power_supply_core.o

ifeq ($(CONFIG_SYSFS),y)
power_supply-objs += power_supply_sysfs.o
endif

ifeq ($(CONFIG_LEDS_TRIGGERS),y)
power_supply-objs += power_supply_leds.o
endif

ifeq ($(CONFIG_POWER_SUPPLY_DEBUG),y)
EXTRA_CFLAGS += -DDEBUG
endif

obj-$(CONFIG_POWER_SUPPLY)	+= power_supply.o

obj-$(CONFIG_PDA_POWER)		+= pda_power.o
obj-$(CONFIG_APM_POWER)		+= apm_power.o
obj-$(CONFIG_WM831X_POWER)	+= wm831x_power.o
obj-$(CONFIG_WM8350_POWER)	+= wm8350_power.o

obj-$(CONFIG_BATTERY_DS2760)	+= ds2760_battery.o
obj-$(CONFIG_BATTERY_DS2782)	+= ds2782_battery.o
obj-$(CONFIG_BATTERY_DS2784)	+= ds2784_battery.o
obj-$(CONFIG_BATTERY_PMU)	+= pmu_battery.o
obj-$(CONFIG_BATTERY_OLPC)	+= olpc_battery.o
obj-$(CONFIG_BATTERY_TOSA)	+= tosa_battery.o
obj-$(CONFIG_BATTERY_WM97XX)	+= wm97xx_battery.o
obj-$(CONFIG_BATTERY_BQ27x00)	+= bq27x00_battery.o
obj-$(CONFIG_BATTERY_DA9030)	+= da9030_battery.o
obj-$(CONFIG_BATTERY_MAX17040)	+= max17040_battery.o
obj-$(CONFIG_CHARGER_PCF50633)	+= pcf50633-charger.o

ifeq ($(CONFIG_MACH_MSM7X27_ALOHAV),y)
	BATT_DRIVER = msm_battery_alohav.o
endif

#
#ADD VS740 BATT DRIVER temporalily
#2010-05-13, taehung.kim
ifeq ($(CONFIG_MACH_MSM7X27_THUNDERC),y)
	BATT_DRIVER = msm_battery_thunderc.o
endif

ifeq ($(CONFIG_MACH_MSM7X27_GISELE),y)
	BATT_DRIVER = msm_battery_gisele.o
endif
BATT_DRIVER ?= msm_battery.o
msm_batt-objs := $(BATT_DRIVER)
obj-$(CONFIG_BATTERY_MSM)	+= msm_batt.o

obj-$(CONFIG_MAX17040_FUEL_GAUGE)	+= max17040.o
