# OnePlus6T Custom Rom Flashing Guide

<p align="center"><img src="./images/screen_capture.png" width="350px"></p>

## 前言

有幾個常見Terms想記低先，事關自己記性真心差，經常轉個頭就唔記得嘢。

OOS = Oxygen OS嘅縮寫。

A/B partition = 算係新嘢嚟，用嚟實現seamless system update，下面會詳細講。

Encryption = 唔係咩新嘢，Android 5.0 已經support full system encryption。

Seamless update = 無縫系統更新，OTA更新嗰陣唔需要打斷當前進行嘅Task

Bootleggers = Rom一個，Slogan係「Trying to make you feel like 家」。注意我提供嘅Bootleggers係Force Encryption Version （⚠已存在喺/data partition嘅舊Data會被格式化，/data分區強制加密⚠）。

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

另外有一個GUI tools叫msmdownloadtool，不過我自已試過，唔係好work（汗）
有興趣可以google下，不過我比較信上面嘅commnad-line tools多啲。

```powershell
https://www.google.com/search?client=firefox-b-d&q=msmdownloadtool+oneplus+6t
```

=======================================================================================

### Oneplus 6T 變磚點算? How to Unbrick?

變磚一貫（我諗亦都係最後）手段係用所謂「線刷」，
