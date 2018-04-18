# -*- encoding: utf-8 -*-
# Copyright (c) 2017, 青岛中怡智能安全研究院有限公司
# All rights reserved
TARBALL_FILENAME=ibmtpm1119.tar.gz
PATCHES=$(wildcard *.patch)
# Note:
# 1. Unzip the upstream source tarball;
# 2. Apply local patches;
# 3. Call another make command to build everything;
.PHONY: all
all:
	$(RM) -r build
	mkdir -p build
	tar axf $(TARBALL_FILENAME) -C build
	cd build && \
	if test "x$(PATCHES)" != "x" ; then for file in "$(PATCHES)" ; do patch -Np1 < ../$${file} ; done ; fi
	$(MAKE) -C build/src -j$$(nproc)
