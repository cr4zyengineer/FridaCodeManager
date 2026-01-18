# Makefile
#
# Compile all FridaCodeManager essentials
# :3
#

SHELL := /var/jb/bin/bash

all: prepare libfcm-compile

prepare:
	@if [ -d lib/build ]; then \
		rm -rf lib/build; \
		mkdir lib/build; \
	else \
		mkdir lib/build; \
	fi

libfcm-compile:
	@$(MAKE) -C libfcm all
	@cp libfcm/tmp/lib/libfcm.a lib/build/libfcm.a
	@$(MAKE) -C libfcm clean

clean:
	@rm -rf lib/build
