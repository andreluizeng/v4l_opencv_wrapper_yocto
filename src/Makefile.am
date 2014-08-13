bin_PROGRAMS = camera_test

camera_test_SOURCES = camera_test.c ../include/v4l_wrapper.h
nodist_camera_test_SOURCES = ../src/v4l_wrapper.c

ROOTFS_DIR = $(SDKTARGETSYSROOT)

TARGET_PATH_LIB 	= $(ROOTFS_DIR)/usr/lib
TARGET_PATH_INCLUDE 	= $(ROOTFS_DIR)/usr/include

AM_CPPFLAGS = -I $(prefix)/usr/src/kernel/include/uapi -I $(prefix)/usr/src/kernel/include/ -I $(TARGET_PATH_INCLUDE) -I ../include


AM_LDFLAGS = -Wl,--library-path=$(TARGET_PATH_LIB),-rpath-link=$(TARGET_PATH_LIB) -lm \
	     -L $(prefix)/usr/lib 

	     
all:
	mv ../src/$(bin_PROGRAMS) ../bin
	
clean-local: 
	rm -rf ../bin/*
	rm -rf ../src/*.o
	