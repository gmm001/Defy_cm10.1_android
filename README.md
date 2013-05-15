Defy_cm10.1_android
===================

Quarx2k Defy cm10.1 repo



---------------------
Quarx2k Defy CM10.1源码同步方法


repo init -u git://github.com/gmm001/android.git -b cm-10.1

repo sync -j16

之后进入.repo/manifests 把local_manifest.xml 拿出来放到.repo 之后同步就OK



或者直接下载，下载后得到的default.xml和local_manifest.xml

把default.xml放入 .repo/manifests 文件夹内
把local_manifest.xml 放入 .repo 文件夹内

repo sync -j16  同步

之后就可以编译了
. build/envsetup.sh 

lunch cm_mb526-userdebug

make -j16 bacon 

一般正常的话2~4个小时吧，由于我去除了语言，所以2个小时，机器I5，8G内存

最近看到好多都在学习同步源码，写出这个给大家学习
