**1. Downloading specific scene from a youtube vid**

    ffmpeg -i $(youtube-dl -f best --get-url "insert-youtube-url") \
    
    -ss 0:17 -t 10 outputfile.mp4

   Syntax:
   
   0:17 = start time of the scene
  
   10 = lenght of scene in seconds
