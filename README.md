# caffe_ocr_for_linux

> 说明：感谢senlinuc贡献的https://github.com/senlinuc/caffe_ocr  
> 我这里的是linux版本，用caffe的master分支合并的。  
> 测试环境 ubuntu 16.04 、cuda 8.0、cudnn 5.1  
1. 需要先安装warp-ctc,https://github.com/ChWick/warp-ctc/tree/develop  
2. 安装完warp-ctc,/usr/local/include/下可能没有ctcpp.h，你可以从源码里复制一份过去
3. 对比下Makefile.config.example文件就知道我改了哪些了环境，你可能需要根据你自己的环境更改下，然后make编译就可以了。
4. 测试程序最终会编译在./build/tools/ocr_test 
5. 如果测试程序输出是乱码，那就看看你的系统默认字符集是什么，senlinux提供的label.txt文件是ANSI的，你可能需要转换下在使用，我的系统是UTF-8，我就把label文件转成了UTF-8，就没有乱码了
