#LED デバイスドライバー(課題1)  
・このデバイスドライバーは2021年度、ロボットシステム学の第7回～第8回の授業内で上田先生が作成したデバイスドライバーを改良したものである。

＃動作環境  
・Raspberry pi 4 model B  
・OS: ubuntu 20.04.3 LTS  


#使用したもの  
・Raspberry pi 4 model B  
・青色LED × 3  
・抵抗120Ω × 3  
・サンハヤト SAD-101 ニューブレッドボード  
・ジャンパ戦 (オス-メス) × 6  


#回路図　　　　
![EPSON001](https://user-images.githubusercontent.com/92074076/146102391-745d32bd-ee30-47b6-9278-a9252a092b44.JPG)  

#配線図　
![写真 2021-12-15 2 33 28](https://user-images.githubusercontent.com/92074076/146102575-dc29f36f-8f6b-4149-b6ae-3f1180e335e2.jpg)　　

#Raspberry pi 4 model B ピン情報
![写真 2021-12-15 9 06 34](https://user-images.githubusercontent.com/92074076/146102730-a546b294-07fd-4479-9a73-1182afaac0f3.png)  「引用元」https://www.raspberrypi.com/documentation/computers/os.html  


#動作方法  
まず、[https://github.com/Takuya0510/myled] に置いてある、Makefileとmake.cをubuntu環境のRaspberry pi 4 model Bの中に作成します。　
次に次のようなコマンドを実行します。  
$ make  
$ sudo insmod myled.ko  
$ sudo chmod 666 /dev/myled0  


実行できたら、次のようなコマンドでLEDを点灯したり消灯したりすることができます。

・すべてのLEDを消灯　　
$ echo 0 >/dev/myled  

・LED1を点灯
$ echo 1 >/dev/myled  

・LED2を点灯
$ echo 2 >/dev/myled  

・LED3を点灯
$ echo 3 >/dev/myled  

・すべてのLEDを点灯
$ echo 4 >/dev/myled  

・LED1を消灯
$ echo 5 >/dev/myled  

・LED2を消灯
$ echo 6 >/dev/myled  

・LED3を消灯
$ echo 7 >/dev/myled 

使用し終わったら次のようなコマンドを実行してください。  
$ sudo rmmod myled  


#実行動画　


#ライセンス　　























