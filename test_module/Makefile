KERN_DIR =/home/at1a5/raspberrypi_dev/linux_4_19
PWD:=$(shell pwd)
obj-m   += test_mem.o
all:
	make ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf- -C $(KERN_DIR) M=$(PWD) modules
clean:
	rm -rf *.o *.ko *.order *.mod.c

send:
	sshpass -p "'" scp test_mem.ko  root@192.168.2.107:/root/
