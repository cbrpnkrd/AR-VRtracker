#
#             LUFA Library
#     Copyright (C) Dean Camera, 2013.
#
#  dean [at] fourwalledcubicle [dot] com
#           www.lufa-lib.org
#
# --------------------------------------
#         LUFA Project Makefile.
# --------------------------------------

# Run "make help" for target help.

MCU          = atmega32u4
ARCH         = AVR8
BOARD        = NONE
F_CPU        = 16000000
F_USB        = $(F_CPU)
OPTIMIZATION = s
TARGET       = GenericHID
SRC          = $(wildcard u8g_src/*.c) $(wildcard sensors/*.c) $(wildcard data/*.c) $(wildcard ahrs/*.c) $(wildcard buttons/*.c) $(TARGET).c Descriptors.c $(LUFA_SRC_USB) $(LUFA_SRC_TWI)
LUFA_PATH    = /home/Finland/AR_VR/AVR/LUFA-130901/LUFA/
U8G_PATH = $(LUFA_PATH)/u8g_src/
CC_FLAGS     = -DUSE_LUFA_CONFIG_HEADER -IConfig/ -Iu8g_src/ -ffunction-sections -fdata-sections
LD_FLAGS     =

# Default target
all:

# Include LUFA build script makefiles
include $(LUFA_PATH)/Build/lufa_core.mk
include $(LUFA_PATH)/Build/lufa_sources.mk
include $(LUFA_PATH)/Build/lufa_build.mk
include $(LUFA_PATH)/Build/lufa_cppcheck.mk
include $(LUFA_PATH)/Build/lufa_doxygen.mk
include $(LUFA_PATH)/Build/lufa_dfu.mk
include $(LUFA_PATH)/Build/lufa_hid.mk
include $(LUFA_PATH)/Build/lufa_avrdude.mk
include $(LUFA_PATH)/Build/lufa_atprogram.mk
