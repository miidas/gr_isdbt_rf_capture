# gr_isdbt_rf_capture
ISDB-Tの受信と再送信  

## 使用機材
#### LEADER LG3802 S1
ISDB-T シグナルジェネレータ

#### Siano SMS2270 USB Dongle
ISDB-T 受信機

#### Lime Microsystems LimeSDR
SDRボード

## Sample Rate設定
8M, 7M, 6Mで復調OK  
5.5Mでもエラーは出るが復調できる  
4MだとRF部がロックしない  

## 実験結果
LG3802 S1でLevelが-50dBmの時の結果を表にまとめた。  

|RX Gain|TX Gain|SNR|RSSI|
| :---: | :---: |:-:|:--:|
|60dB|20dB|23dB|-50dBm|
|60dB|10dB|23dB|-60dBm|
|60dB| 0dB|22dB|-65dBm|
|50dB|40dB|30dB|-40dBm|
|50dB|30dB|30dB|-50dBm|
|50dB|10dB|30dB|-60dBm|
|50dB|10dB|30dB|-65dBm|
|50dB| 0dB|22dB|-65dBm|
|40dB|50dB|30dB|-40dBm|
|40dB|40dB|30dB|-50dBm|
|40dB|30dB|30dB|-60dBm|
|40dB|20dB|28dB|-65dBm|
|40dB|10dB|22dB|-65dBm|
|30dB|50dB|28dB|-50dBm|
|30dB|40dB|28dB|-60dBm|
|30dB|30dB|25dB|-65dBm|
|30dB|20dB|20dB|-65dBm|

## 注意点
Oversampleの値を上げておかないとSNRが落ちる。 (Oversample=1のとき5dB程度)
