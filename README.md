node-rtsp-stream
================

** NOTE **
This is a fork of the Node RTSP Stream library found at https://github.com/kyriesent/node-rtsp-stream. This fork is simply to modify the FFMPeg command arguments to improve video playback of a stream in the Google Chrome web browser.

Stream any RTSP stream and output to websocket for consumption by [jsmpeg](https://github.com/phoboslab/jsmpeg). HTML5 streaming video! (Requires ffmpeg)

Usage:

```
$ npm install mikesappshop-node-rtsp-stream
```

On server:
```
Stream = require('mikesappshop-node-rtsp-stream');
stream = new Stream({
    name: 'name',
    streamUrl: 'rtsp://184.72.239.149/vod/mp4:BigBuckBunny_115k.mov',
    wsPort: 9999
});
    
```

On client:
```
client = new Websocket('ws://localhost:9999');
player = new jsmpeg(client, {
    canvas: canvas // Canvas should be a canvas DOM element
});

```

For more information on how to use jsmpeg to stream video, visit https://github.com/phoboslab/jsmpeg
