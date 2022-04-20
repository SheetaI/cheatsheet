**1. Downloading specific scene from a youtube vid**

- Enter:
        
   `ffmpeg -i $(youtube-dl -f best --get-url "insert-youtube-url") \`
        
- Followed by:

   `-ss 0:17 -t 10 -c copy outputfile.mp4`

   Syntax:
   
   0:17 = start time of the scene
  
   10 = lenght of thescene in seconds
