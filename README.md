RoboSys homework1
===

## 概要
* LEDを点灯させるデバイスドライバです。  
* /dev/myled0に1を書き込むとLEDが光り0を書き込むとLEDが消灯します。
* old_Makefile を使用してmakeすることも可能

## 使用環境
Raspberry pi3  
OS: Raspbian (ubuntu16.04.5 LTS)  
カーネル再構築はしてあることが前提    
ubuntu の場合, 環境構築の前に以下のコマンドを実行    
* `$ sudo apt install linux-headers-$(uname -r)`  
* ubuntu_Makefile を使用してmakeすること  

## 環境構築
```
$ git clone https://github.com/bulauza/robosys.git
$ cd robosys/
$ make
$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0
```

## 実行方法
* LED点灯
  * `$ echo 1 > /dev/myled0`
* LED消灯
  * `$ echo 0 > /dev/myled0`
* LEDフェードイン
  * `$ echo 2 > /dev/myled0`
* LEDフェードアウト
  * `$ echo 3 > /dev/myled0`

## 後始末
```
$ sudo rmmod myled.ko
$ make clean
```

## 動画
https://m.youtube.com/watch?v=eryEZQW-6hU

## 参考にしたサイト
https://github.com/ryuichiueda/robosys2018/blob/master/06.md  
https://qiita.com/take-iwiw/items/1fdd2e0faaaa868a2db2  
https://prev.net-newbie.com/linux/driver/driver2.html
