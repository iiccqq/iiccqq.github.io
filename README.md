"# site" 


ffmpeg -f dshow -i video="Integrated Camera" 2.mp4 -t 20
ffmpeg -f dshow -i video="Integrated Camera"  -codec:v libx264 -codec:a mp3 -map 0 -f ssegment -segment_format mpegts -segment_list playlist.m3u8 -segment_time 10 out%03d.ts

