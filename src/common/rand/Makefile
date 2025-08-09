#When the Gnu Make is not available,simply comment out
#the lines defining the test of OS:
#   ifeq ($(OS),Darwin)
#      LDFLAGS += -L/opt/local/lib -lusb-1.0
#   endif
#
#When running on Mac OS X system, please define the variable
#"OS" with the value "Darwin" by running the command
#"make OS=Darwin"
LIB_AND_APPS_PATH = ../../Libs-Apps/
QUANTIS_LIB_PATH = $(LIB_AND_APPS_PATH)build/Quantis
QUANTIS_EXT_LIB_PATH = $(LIB_AND_APPS_PATH)build/QuantisExtensions
QUANTIS_INC_PATH = $(LIB_AND_APPS_PATH)Quantis
QUANTIS_EXT_INC_PATH = $(LIB_AND_APPS_PATH)QuantisExtensions


CFLAGS += -I$(QUANTIS_INC_PATH)
CFLAGS += -I$(QUANTIS_EXT_INC_PATH)
CFLAGS += -O3
LDFLAGS = -lusb-1.0 -L$(QUANTIS_LIB_PATH) -lQuantis -pthread
#LDFLAGS = -lusb-1.0 -lQuantis -pthread
#LDFLAGS += -L$(QUANTIS_EXT_LIB_PATH) -lQuantis_Extensions

ifeq ($(OS),Darwin)
  LDFLAGS += -L/opt/local/lib -lusb-1.0
else
  LDFLAGS += -lrt
endif
