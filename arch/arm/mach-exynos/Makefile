# arch/arm/mach-exynos/Makefile
#
# Copyright (c) 2010-2011 Samsung Electronics Co., Ltd.
#		http://www.samsung.com/
#
# Licensed under GPLv2

obj-y				:=
obj-m				:=
obj-n				:=
obj-				:=

# Core

obj-$(CONFIG_ARCH_EXYNOS)	+= common.o

obj-$(CONFIG_PM_SLEEP)		+= pm.o sleep.o
obj-$(CONFIG_PM_GENERIC_DOMAINS) += pm_domains.o

obj-$(CONFIG_ARCH_EXYNOS)	+= pmu.o

obj-$(CONFIG_SMP)		+= platsmp.o headsmp.o

obj-$(CONFIG_HOTPLUG_CPU)	+= hotplug.o

obj-$(CONFIG_ARCH_EXYNOS)	+= exynos-smc.o
obj-$(CONFIG_ARCH_EXYNOS)	+= firmware.o

plus_sec := $(call as-instr,.arch_extension sec,+sec)
AFLAGS_exynos-smc.o		:=-Wa,-march=armv7-a$(plus_sec)

# machine support

obj-$(CONFIG_ARCH_EXYNOS4)	+= mach-exynos4-dt.o
obj-$(CONFIG_ARCH_EXYNOS5)	+= mach-exynos5-dt.o
