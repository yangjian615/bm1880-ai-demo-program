1. Get models:
https://sophon-file.bitmain.com.cn/sophon-prod/drive/18/11/04/15/models.7z.zip

2. Uncompress the models.7z.zip in the darknet folder.

3. Modify the Makefile in darknet folder.
	a. CC set to your 1880 toolchain path(aarch64-linux-gnu-gcc)
	b. AR set to your 1880 toolchain path(aarch64-linux-gnu-ar )
	c. COMMON set to your 1880 include path

4. cd darknet-yolov2-object-classification/darknet then:  make MODE=SOC

5. copy the whole darknet-yolov2-object-classification to your usb if your board is running on usb host mode. or you can copy the whole darknet-yolov2-object-classification folder to your sdcard rootfs partition 

6. when booting up your 1880 board, vi the demo.sh ,and change the DEMO_DIR to your darknet-yolov2-object-classification path. you need also change the pushd/popd command to "cd" command

7. cd to the darknet-yolov2-object-classification folder and  run the command: ./demo.sh images/
