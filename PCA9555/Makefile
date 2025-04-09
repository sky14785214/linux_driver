obj-m += pca9555.o

KDIR ?= /lib/modules/$(shell uname -r)/build

PWD := $(shell pwd)

OUTPUT_DIR := $(PWD)/output  # 定義輸出目錄

all:
	$(MAKE) -C $(KDIR) M=$(PWD) modules
	mkdir -p $(OUTPUT_DIR)  # 建立輸出目錄（如果不存在）
	cp pca9555.ko $(OUTPUT_DIR)  # 將 .ko 檔案複製到輸出目錄

clean:
	$(MAKE) -C $(KDIR) M=$(PWD) clean
	rm -f $(OUTPUT_DIR)/pca9555.ko  # 移除輸出目錄中的 .ko 檔案