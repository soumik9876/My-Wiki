
<p align="center">
	<img src="https://github.com/Saurav-Paul/My-Wiki/blob/master/logo.png" align="center" >
</p>

<h1 align="center">my wiki</h1>
<h4 align="center"><i>Informations & tutorials</i> </h4>

---



## ScreenRecording with Ffmpeg

*It is really a very nice tool for converting videos. Also it can record screencast.*

## Commands for recording video

*It will record video with audio**

> ffmpeg -f alsa -ac 2 -i pulse -f x11grab -r 25 -s 1366x768 -i :0.0 \
-vcodec libx264 -pix_fmt yuv420p -preset ultrafast -crf 0 -threads 0 \
-acodec pcm_s16le -y output.mkv


*For recording video without audio, write the given command*
> ffmpeg -f x11grab -r 25 -s 1366x768 -i :0.0 \
-vcodec libx264 -pix_fmt yuv420p -preset ultrafast -crf 0 -threads 0 \
-acodec pcm_s16le -y output.mkv

**To know your screen resulation, write the given command**

> xdpyinfo | awk '/dimensions/{print $2}'


## Convertion

*Convert into GIF*

> ffmpeg -i input.mkv output.gif
