# GNU make Makefile template for individual componets
# Copyrights (c) Huawei Technologies (I) Pvt. Ltd.

#include the common MiniSip code organization definitions
#include $(SS_CODE_BUILD)/make.minisip.defs.mk
include ../make.minisip.defs.mk

# Include a common definition file
#include $(SS_CODE_BUILD)/makedefs.minisip.mk
include ../makedefs.minisip.mk

# Set up the include folder directory with Internal headers of the component
SS_CBB_INCLUDES = $(SS_CC_INCLUDE)$(SS_CBB_DIR)/$(SS_INCLUDE_DIR)\
                  $(SS_CC_INCLUDE)$(SS_CBB_DIR)/$(SS_H_DIR)\
                  $(SS_CC_INCLUDE)$(SS_CBB_DIR)/$(SS_INC_DIR)

# Source Location
SS_CBB_SRC_DIR = $(SS_CBB_DIR)/$(SS_SRC_DIR)


# External Interface headers files exposed by this component
SS_CBB_INCLUDE_DIR     = $(SS_CBB_DIR)/$(SS_INCLUDE_DIR)
SS_CBB_LIB_DEBUG_DIR   = $(SS_LIB_DEBUG_DIR)
SS_CBB_LIB_RELEASE_DIR = $(SS_LIB_RELEASE_DIR)
SS_CBB_OBJ_DEBUG_DIR   = $(SS_CBB_OBJ_DIR)/debug
SS_CBB_OBJ_RELEASE_DIR   = $(SS_CBB_OBJ_DIR)/release

# Transaction Object List
SS_CBB_DEBUG_OBJS =  \
	$(SS_CBB_OBJ_DEBUG_DIR)/vppmemcp.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_DEBUG_DIR)/vpplist.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_DEBUG_DIR)/vppset.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_DEBUG_DIR)/vpphash.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_DEBUG_DIR)/vppipaddr.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_DEBUG_DIR)/vpphashutil.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_DEBUG_DIR)/vpptoken.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_DEBUG_DIR)/vppstring.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_DEBUG_DIR)/vppmsgcb.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_DEBUG_DIR)/vppstrbuf.$(SS_OBJ_SUFFIX)

SS_CBB_RELEASE_OBJS =  \
	$(SS_CBB_OBJ_RELEASE_DIR)/vppmemcp.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_RELEASE_DIR)/vpplist.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_RELEASE_DIR)/vppset.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_RELEASE_DIR)/vpphash.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_RELEASE_DIR)/vppipaddr.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_RELEASE_DIR)/vpphashutil.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_RELEASE_DIR)/vpptoken.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_RELEASE_DIR)/vppstring.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_RELEASE_DIR)/vppmsgcb.$(SS_OBJ_SUFFIX) \
	$(SS_CBB_OBJ_RELEASE_DIR)/vppstrbuf.$(SS_OBJ_SUFFIX)


# Common Targets

all: $(SS_CBB_DEBUG_OBJS) $(SS_CBB_RELEASE_OBJS)
	$(call SS_ARCHIVE,$(SS_CBB_LIB_DEBUG_DIR),$(SS_CBB_DEBUG_OBJS),$(SS_CBB_LIB))
	$(call SS_ARCHIVE,$(SS_CBB_LIB_RELEASE_DIR),$(SS_CBB_RELEASE_OBJS),$(SS_CBB_LIB))

clean:
	$(SS_RMV) $(SS_CBB_OBJ_DEBUG_DIR)/*.$(SS_OBJ_SUFFIX)
	$(SS_RMV) $(SS_CBB_OBJ_RELEASE_DIR)/*.$(SS_OBJ_SUFFIX)
	$(SS_RMV) $(SS_CBB_LIB_DEBUG_DIR)/*.$(SS_LIB_SUFFIX)
	$(SS_RMV) $(SS_CBB_LIB_RELEASE_DIR)/*.$(SS_LIB_SUFFIX)

cleanlib:
	$(SS_RMV) $(SS_CBB_LIB_DEBUG_DIR)/*.$(SS_LIB_SUFFIX)
	$(SS_RMV) $(SS_CBB_LIB_RELEASE_DIR)/*.$(SS_LIB_SUFFIX)


# DEBUG OBJECTS BUILDING RULES
$(SS_CBB_OBJ_DEBUG_DIR)/vppmemcp.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vppmemcp.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_DEBUG),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_DEBUG_DIR),vppmemcp)

$(SS_CBB_OBJ_DEBUG_DIR)/vpplist.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vpplist.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_DEBUG),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_DEBUG_DIR),vpplist)

$(SS_CBB_OBJ_DEBUG_DIR)/vppset.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vppset.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_DEBUG),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_DEBUG_DIR),vppset)

$(SS_CBB_OBJ_DEBUG_DIR)/vpphash.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vpphash.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_DEBUG),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_DEBUG_DIR),vpphash)

$(SS_CBB_OBJ_DEBUG_DIR)/vppipaddr.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vppipaddr.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_DEBUG),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_DEBUG_DIR),vppipaddr)

$(SS_CBB_OBJ_DEBUG_DIR)/vpphashutil.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vpphashutil.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_DEBUG),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_DEBUG_DIR),vpphashutil)

$(SS_CBB_OBJ_DEBUG_DIR)/vpptoken.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vpptoken.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_DEBUG),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_DEBUG_DIR),vpptoken)

$(SS_CBB_OBJ_DEBUG_DIR)/vppstring.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vppstring.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_DEBUG),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_DEBUG_DIR),vppstring)

$(SS_CBB_OBJ_DEBUG_DIR)/vppmsgcb.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vppmsgcb.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_DEBUG),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_DEBUG_DIR),vppmsgcb)

$(SS_CBB_OBJ_DEBUG_DIR)/vppstrbuf.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vppstrbuf.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_DEBUG),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_DEBUG_DIR),vppstrbuf)


# Release Object building rules
$(SS_CBB_OBJ_RELEASE_DIR)/vppmemcp.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vppmemcp.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_RELEASE),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_RELEASE_DIR),vppmemcp)

$(SS_CBB_OBJ_RELEASE_DIR)/vpplist.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vpplist.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_RELEASE),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_RELEASE_DIR),vpplist)

$(SS_CBB_OBJ_RELEASE_DIR)/vppset.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vppset.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_RELEASE),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_RELEASE_DIR),vppset)

$(SS_CBB_OBJ_RELEASE_DIR)/vpphash.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vpphash.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_RELEASE),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_RELEASE_DIR),vpphash)

$(SS_CBB_OBJ_RELEASE_DIR)/vppipaddr.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vppipaddr.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_RELEASE),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_RELEASE_DIR),vppipaddr)

$(SS_CBB_OBJ_RELEASE_DIR)/vpphashutil.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vpphashutil.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_RELEASE),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_RELEASE_DIR),vpphashutil)

$(SS_CBB_OBJ_RELEASE_DIR)/vpptoken.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vpptoken.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_RELEASE),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_RELEASE_DIR),vpptoken)

$(SS_CBB_OBJ_RELEASE_DIR)/vppstring.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vppstring.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_RELEASE),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_RELEASE_DIR),vppstring)

$(SS_CBB_OBJ_RELEASE_DIR)/vppmsgcb.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vppmsgcb.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_RELEASE),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_RELEASE_DIR),vppmsgcb)

$(SS_CBB_OBJ_RELEASE_DIR)/vppstrbuf.$(SS_OBJ_SUFFIX): $(SS_CBB_SRC_DIR)/vppstrbuf.$(SS_SRC_SUFFIX)
	$(call SS_COMPILE,$(SS_CFLAGS_RELEASE),$(SS_CBB_INCLUDES),$(SS_CBB_SRC_DIR),$(SS_CBB_OBJ_RELEASE_DIR),vppstrbuf)

