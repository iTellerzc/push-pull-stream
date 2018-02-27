本项目需安装
1.npm
2.nodejs
3.bower(可选)
4.ffmpeg
------------------------
1.安装ws依赖
npm install ws
2.启动项目
node stream-server.js 1234 pushPort pullPort
3.ffmpeg 推流
ffmpeg -s 640×480 -f dshow -i video="Webcam C170" -f mpeg1video -b:v 400k -r 30 http://192.168.1.83:8082/1234/640/480/
4.测试
打开 stream-example.html 即可获取视频流
5.查看可用设备
ffmpeg -list_devices true -f dshow -i dummy