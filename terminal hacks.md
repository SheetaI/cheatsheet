**1. Downloading specific scene from a youtube vid**

- Enter:
        
   `ffmpeg -i $(youtube-dl -f best --get-url "insert-youtube-url") \`
        
- Followed by:

   `-ss 0:17 -t 10 -c copy outputfile.mp4`

   Syntax:
   
   0:17 = start time of the scene
  
   10 = lenght of thescene in seconds

**2. Zoom-in Zoom-out**

   `Super + Shift + Up/Down Keys`

**3. Speeding up a video**

 `ffmpeg -i input.mp4 -filter:v "setpts=0.25*PTS" output.mp4`

 `ffmpeg -i input.mkv -filter_complex "[0:v]setpts=0.5*PTS[v];[0:a]atempo=2.0[a]" -map "[v]" -map "[a]" output.mkv`

**4. Cut a video**

 `ffmpeg -i input.mp4 -ss 0:02 -t 22 -c copy output.mp4`
