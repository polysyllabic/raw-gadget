# SPDX-License-Identifier: Apache-2.0

obj-m := raw_gadget.o
KDIR := /lib/modules/$(shell uname -r)/build
PWD := $(shell pwd)

default:
	$(MAKE) -C $(KDIR) M=$(PWD) SUBDIRS=$(PWD) modules

install:
	sudo install -d /usr/local/modules
	sudo install -C insmod.sh raw_gadget.ko /usr/local/modules

clean:
	$(MAKE) -C $(KDIR) M=$(PWD) SUBDIRS=$(PWD) clean
