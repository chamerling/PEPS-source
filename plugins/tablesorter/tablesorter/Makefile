########################################
# USER VARIABLES
MKLIB ?= opa-plugin-builder
PLUGNAME = tablesorter.opp
SRC = jquery.tablesorter.js tablesorter.js
CONF =

########################################
# MAKEFILE VARIABLES
ifeq ($(origin BUILDDIR), undefined)
	PWD := $(shell pwd)
	BUILDDIR := $(PWD)/_build/
	export BUILDDIR
endif

########################################
# PLUGIN BUILDING
$(PLUGNAME) : $(SRC)
	@echo "### Building plugin $(PLUGNAME)"
	$(MKLIB) --js-validator-off -o $(@:%.opp=%) $? $(CONF) --build-dir $(BUILDDIR)

########################################
# CLEANING
clean :
	@echo "### Cleaning plugin $(PLUGNAME)"
	@rm -rf $(BUILDDIR)/$(PLUGNAME)

