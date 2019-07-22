# OnePlus6T Custom Rom Flashing Guide

<p align="center"><img src="./images/screen_capture.png" width="350px"></p>
   
## 前言

有幾個常見Terms想記低先，事關自己記性真心差，經常轉個頭就唔記得嘢。

OOS = Oxygen OS嘅縮寫。

A/B partition = 算係新嘢嚟，用嚟實現seamless system update，下面會詳細講。

Encryption = 唔係咩新嘢，Android 5.0 已經support full system encryption。

Seamless update = 無縫系統更新，OTA更新嗰陣唔需要打斷當前進行嘅Task。

OTA升級 = Over-The-Air，線上收到Push包升級，都會簡單講下。

Bootleggers = Rom一個，Slogan係「Trying to make you feel like 家」。注意提供嘅Bootleggers係Force Encryption Version （⚠已存在喺/data partition嘅舊Data會被格式化，/data分區強制加密⚠）。

=======================================================================================

下面提供我依家用緊嘅Packages，Download link 係google drive嚟 (因為太大放唔到上github)。

| Rom Packages DL Link   | **Include Packages**                                         |
| ---------------------- | ------------------------------------------------------------ |
| https://bit.ly/2JTBjCq | BootleggersROM-Pie (fajita) 4.2 stable - [20190614-08:45:11 Build] |
|                        | OnePlus6T Oxygen 34 OTA (Strock Rom)                         |
|                        | Open GApps ARM64 9.0 Pico                                    |
|                        | TWRP 3.3.1-1 (fajita) Image                                  |
|                        | TWRP 3.3.1-0 (fajita) Installer                              |
|                        | Magisk-v19.3 (Force Encryption)                              |

| Unbrick tools DL Link <br/>(For Windows, command-line) | Include Packages                                     |
| ------------------------------------------------------ | ---------------------------------------------------- |
| http://bit.ly/2OaijoI                                  | OnePlus6T Oxygen 34 OTA (FASTBOOT Flashing firmware) |
|                                                        | adb.exe & fastboot.exe & more misc required tools    |

另外有一個GUI tools叫[msmdownloadtool](https://www.google.com/search?client=firefox-b-d&q=msmdownloadtool+oneplus+6t)，不過我自已試過，唔係好work（汗）
有興趣可以google下，不過我比較信上面嘅commnad-line tools多啲。

=======================================================================================



## OTA（Over-The-Air）系統升級







## 究竟乜嘢係A/B partition?











## Oneplus 6T 變磚點算 ? How to Unbrick?

變磚一貫（我諗亦都係最後）一道防線係用所謂「線刷」。簡單嚟講就係要用到你部電腦，有一個work嘅rom image（對應好哂partition），然後將部brick咗嘅機入Fastboot mode，用usb線連fastboot直接寫入去flash到。具體操作係配合adb shell用dd if=xxx of=xxx command。



#### Windows上嘅Unbrick工具

主要都係用翻上面條DL Link嗰個Tools (另一個叫「msmdownloadtool」嘅我自己就失敗咗，有興趣可以自行研究)。呢個方法適用於Windows，不過其實Linux都係差唔多咁上下，都係照跟翻fastboot command 寫成script，有機會遲啲再寫個。

解壓咗`9.0.12-OnePlus6TOxygen_34_OTA_019_all_1901231347_fb09dd2d4-FASTBOOT.zip`之後>`Others_flashall` > `flash-all-partitions.bat`

Run呢個batch scrtip，之後都係跟住prompt instruction，同埋等就ok。你會見到佢係將A/B partition都flash翻stock rom落去，以及stock recovery。
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

## References:

https://forum.xda-developers.com/oneplus-6/how-to/guide-noobs-guide-to-b-partitions-op6-t3816123

https://www.xda-developers.com/how-a-b-partitions-and-seamless-updates-affect-custom-development-on-xda/

https://forum.xda-developers.com/oneplus-6t/help/bricked-oneplus-6t-msmdownloadtool-t3900145
