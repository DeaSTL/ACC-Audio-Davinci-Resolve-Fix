# ACC-Audio-Davinci-Resolve-Fix
You're welcome...


For all of those that are having trouble getting audio working on ACC encoded video files here the solution.
This has been tested on one system so far so this goes without saying but 
###I AM NOT RESPONSIBLE FOR BREAKING YOUR VIDEO FILES, MAKE A BACKUP BEFORE USING THIS

## Install this stuff first

So you're going to need python, ffmpeg, and git
```
sudo apt install python3 ffmpeg git
git clone https://github.com/DeaSTL/ACC-Audio-Davinci-Resolve-Fix.git
```
Then you may want to to make a alias of this script in your ` ~/.bashrc` file
like so
```
vim ~/.bashrc
And add the line at the bottom
alias convertaudio="/path/to/repo/convertaudio"
```
If you don't want to do this then you can also just copy the convertaudio file to the directory you want to convert.


##How to use?
Simply run the command `convertaudio` in the directory with the mp4s you want to convert(Did I mention it only works with mp4s, so yeah...)
After it's complete it will output `Audio extraction and combination complete. Temporary directory deleted.`
This is by far much faster than using something like handbrake because it doesn't touch the video encoding, excellent for large 4k video files like i'm dealing with.


##How it works?
This starts by extracting the audio and converting it to opus audio encoding, then it will take that audio file and create a video file of the source video and the opus audio making it possible to use ACC encoded mp4s in Davinci Resolve like the ones outputted from OBS and a GoPro.

Note that the script will create `./output/` , this is where your new mp4s will be stored.


