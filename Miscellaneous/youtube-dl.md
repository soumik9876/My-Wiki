
<p align="center">
	<img src="https://github.com/Saurav-Paul/My-Wiki/blob/master/logo.png" align="center" >
</p>

<h1 align="center">my wiki</h1>
<h4 align="center"><i>Informations & tutorials</i> </h4>

---





## Youtube Video Downloader : youtube-dl

**youtube-dl is a command-line program to download videos from YouTube.com and a few more sites.**

## Installation
sudo curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl

sudo chmod a+rx /usr/local/bin/youtube-dl

or, 
sudo wget https://yt-dl.org/downloads/latest/youtube-dl -O /usr/local/bin/youtube-dl

sudo chmod a+rx /usr/local/bin/youtube-dl

or,
sudo pip install --upgrade youtube_dl

or,
brew install youtube-dl



### Also download ffmpeg

## Download videos

youtube-dl url

for getting all format 
youtube-dl -F url

for download certain format 
youtube-dl -f number url

dorwnload in best possible audio+video format
youtube-dl -f best url

youtube-dl -f bestvideo+bestaudio url

youtube-dl -f 'bestvideo[ext=mp4]+bestaudio[ext=m4a]' url

## youtube-dl config
Adding this line -f 'bestvideo[ext=mp4]+bestaudio[ext=m4a]' to the ~/.config/youtube-dl/config will help to set defalut
and it also can be ignore very easily by --ignore-config



