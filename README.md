# rpe-ltp
how to use rpe-ltp in your computer?
1.在终端中采用ffmpeg命令： ffmpeg -i input.wav -f s16le -ar 8000 -ac 1 -acodec pcm_s16le AU_output_Encoder_input.pcm  将input.wav转换为AU_output_Encoder_input.pcm文件，因为rpe-ltp要求的输入为PCM后缀的文件，即未封装的语音文件。
2.运行encoder-rpe-ltp，将输入的AU_output_Encoder_input.pcm进行编码，输入为encoder_output.pcm。
3.运行Ed-iface,将encoder_output.pcm转换为ed_iface_output.pcm。
4.运行decoder-rpe-ltp，将ed_iface_output.pcm进行解码，输出decoder_output.pcm。
5.使用Adobe Audition打开decoder_output.pcm文件，选择8000HZ ,单声道，编码16位PCM，字节顺序默认字节顺序（即little-endian 小端模式），开始字节偏移0字节，来进行直接播放。

附上：
ffmpeg的安装链接：https://www.zl-asica.com/2020/ffmpeg/
（注：使用前先进入需要转换的wav文件的目录下）
Adobe Audition的下载链接：https://www.yuque.com/docs/share/c48788a7-e66b-42bf-b318-13b43d113c56?#
