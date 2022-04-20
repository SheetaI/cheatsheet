**ffmpeg**


`ffmpeg -i $(youtube-dl -f best --get-url "insert-youtube-url") \
-ss x:xx -t xx outputfile.mp4`

Syntax:
x:xx = start time of clip # ex: 0:12
xx = lenght of clip in sec. # ex: 10 
