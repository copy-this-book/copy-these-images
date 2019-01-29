Square sTream
=============

Images for social networks.

Even if they only want the jPEG,
it’s still the PNG here sometimes.


Some tech notes
=========

copy gif to mp4:

ffmpeg -i animated.gif -movflags faststart -pix_fmt yuv420p video.mp4

If your animation is too short, you will need to loop it several times: instagram needs at least a ten second video. You can do this with FFMPEG. Create a list.txt file like this:

file 'video.mp4'
file 'video.mp4'
file 'video.mp4'
file 'video.mp4'

Then:

ffmpeg -f concat -i list.txt -c copy video-for-instagram.mp4
