# Install

* Install NodeJS
* Install FFmpeg

# How to run

```
git clone
cd node-video-server
npm install


ffmpeg -hide_banner -fflags nobuffer  -loglevel debug -rtsp_transport tcp -flags -global_header -i rtsp://YOUR_IP:PORT -an -c:v copy -b:v 2048k -f hls -lhls 1 -hls_time 1 -hls_list_size 3 -hls_flags delete_segments -hls_segment_type fmp4 videos/stream.m3u8

node app.js
```

Video will be available at the link:
[localhost:5000/videos/stream.m3u8](localhost:5000/videos/stream.m3u8)