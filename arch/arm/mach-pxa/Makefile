#
# Makefile for the linux kernel.
#

# Common support (must be linked before board specific support)
obj-y += generic.o irq.o dma.o

# Specific board support
obj-$(CONFIG_ARCH_LUBBOCK) += lubbock.o
obj-$(CONFIG_ARCH_PXA_IDP) += idp.o

# Support for blinky lights
led-y := leds.o
led-$(CONFIG_ARCH_LUBBOCK) += leds-lubbock.o
led-$(CONFIG_ARCH_PXA_IDP) += leds-idp.o

obj-$(CONFIG_LEDS) += $(led-y)

# Misc features
obj-$(CONFIG_PM) += pm.o sleep.o
