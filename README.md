# nhentai-one-key-downloader
Please use https://github.com/Tsuk1ko/nhder instead.

请使用 https://github.com/Tsuk1ko/nhder ，本脚本将封存，不再维护

A pure shell script that can easily download comics from nhentai.

一个可以一键下载nhentai本子的纯shell脚本。

[中文说明文档](https://lolico.moe/technology/nhentai-downloader.html)

## Prepare
First, download this script.
```bash
wget -N --no-check-certificate https://raw.githubusercontent.com/YKilin/nhentai-one-key-downloader/master/nhentai-batch.sh && chmod +x nhentai-batch.sh
```
Then edit it with vi or other editor. You can see this part at the beginning of the script.
```bash
#setting  off:0  on:1
zad=1			#Auto zip the directory after downloading
dsaz=1			#Delete sourse directory after zipping

dldir="comics"	#The name of the directory you want to download to (can be ausolute or relative)
```
Modify it according to your needs.

## Start using
There are 2 modes in this script.
### Mode a
Download from an nhentai (search/tags/artists/...) website that include multi comics. Such as `https://nhentai.net/search/?q=xxxxxx`.
```bash
./nhentai-batch.sh -a
```
Then follow the tips input an nhentai website and press enter. The script will analyze all comics on the website automatically.  
After finishing analyzing, the script will remind you that there are 3 modes to download comics:

1. White list mode : Download which you appoint
1. Black list mode : Which you appoint WON'T be downloaded
1. God mode : DOWNLOAD ALL !!!

If you choose mode 1 or 2, you will be ask to input the ordinals of the comics you want (or do not want) to download. (separated them by space)

### Mode b
Download from nhentai websites like `https://nhentai.net/g/xxxxxx/`.
```bash
./nhentai-batch.sh -b
```
Then follow the tips input nhentai websites. Each website end with a Enter. An empty line input means stop continuing input.    
Then the script will download all comic you input automatically.  
**IMPORTANT: There must be a "/" after the url!**

## Other explanation
If you interrupt it while downloading, the download will continue when you download the same comic again.    
If you have interrupted the script while running, you will find directories like `.nhentai-temp-xxxxx`. They are temp files which can be delete.

## TODO
Development a web page.
