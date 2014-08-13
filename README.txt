1 - Creating build files
------------------------

  user@localhost:~/v4l_wrapper/yocto$ autoheader
  user@localhost:~/v4l_wrapper/yocto$ autoreconf --install
  
  
2 - building application
------------------------

  user@localhost:~/v4l_wrapper/yocto$ cd /opt/poky/1.6.1
  
  user@localhost:~/opt/poky/1.6.1$. ./environment-setup-cortexa9hf-vfp-neon-poky-linux-gnueabi
  user@localhost:~/opt/poky/1.6.1$ cd -
  
  user@localhost:~/v4l_wrapper/yocto$ ./configure --host=arm-poky-linux-gnueabi --prefix=$SDKTARGETSYSROOT
  user@localhost:~/v4l_wrapper/yocto$ make
  
3 - note
--------

  a) if you perform the make install command, all the binaries will be placed in your rootfs/usr/bin, if you only enter make, the binaries will be placed
  in the bin/ folder (due a workaround in src/Makefile.am)
  
  b) once exported the yocto's toolchain variables (environment-setup.....) you will need a new terminal (cleaned) if you want to perform all the operations again (autoheader and autoconf).
  
  

  
EOF !
  
  