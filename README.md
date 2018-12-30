RoboSys homework1
===

## 概要
* LEDを点灯させるデバイスドライバです。  
* /dev/myled0に1を書き込むとLEDが光り0を書き込むとLEDが消灯します。

## 環境構築
```
$ 
```

## 実行方法
* LED点灯
  * `$ echo 1 > /dev/myled0`

## 後始末
```
$ sudo rmmod myled.ko
$ make clean
```

## 参考にしたサイト
https://github.com/ryuichiueda/robosys2018/blob/master/06.md  
https://prev.net-newbie.com/linux/driver/driver2.html
