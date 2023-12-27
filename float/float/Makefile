VESC_TOOL ?=/usr/local/bin/vesc_tool_6.02

TARGET = float

SOURCES = float.c footpad_sensor.c konami.c conf/buffer.c conf/confparser.c conf/confxml.c

ADD_TO_CLEAN = conf/confxml.h conf/confxml.c
USE_STLIB = yes
VESC_C_LIB_PATH = ../../c_libs/
include $(VESC_C_LIB_PATH)rules.mk

float.c: conf/confparser.h conf/confxml.h

conf/confparser.h conf/confxml.h conf/confxml.c &: conf/settings.xml
	$(VESC_TOOL) --xmlConfToCode conf/settings.xml
