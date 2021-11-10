## **Real-time video transcoding**

**Video transcoding** is one of the most important steps in the streaming video process, but it can be difficult to facilitate. Video providers must be able to accommodate an increasing number of display devices with screen resolutions and frame rates that creep higher over time. And as devices, resolutions, and frame rates increase, so does the transcoding time required for complex video that is distributed on-demand.

**FFMPEG** is one of the most popular open-source multimedia manipulation tools with a library of plugins that can be applied to various parts of the audio and video processing pipelines and have achieved wide adoption across the world.
Video encoding, decoding and transcoding are some of the most popular applications of FFmpeg.

**Install ffmpeg** - python3 -m pip install ffmpeg-python

**ffmpeg GPU**
https://docs.nvidia.com/video-technologies/video-codec-sdk/ffmpeg-with-nvidia-gpu/

**Installation Steps:**
To compile FFmpeg on Linux, do the following:
1. Clone ffnvcodec 
    git clone https://git.videolan.org/git/ffmpeg/nv-codec-headers.git
2. Install ffnvcodec 
    cd nv-codec-headers && sudo make install && cd ..
3. Clone FFmpeg's public GIT repository. 
    git clone https://git.ffmpeg.org/ffmpeg.git ffmpeg/
4. Install necessary packages. 
    sudo apt-get install build-essential yasm cmake libtool libc6 libc6-dev unzip wget libnuma1 libnuma-dev
5. Configure
    ./configure --enable-nonfree --enable-cuda-nvcc --enable-libnpp --extra-cflags=-I/usr/local/cuda/include --extra-ldflags=-L/usr/local/cuda/lib64
6. Compile 
    make -j 8
7. Install the libraries. 
    sudo make install

**Install x264**
It’s optional step but if we planning using in future regular software encoding also, we need install x264.
- git clone <https://code.videolan.org/videolan/x264.git>
- cd x264/
- ./configure --disable-cli --enable-static --enable-shared --enable-strip
- make
- make install
- ldconfig

The following command reads file input.mp4 and transcodes it to output.mp4 with H.264 video at the same resolution and with the same audio codec.

**Working with:**
ffmpeg -init_hw_device cuda=0 -i test.mp4 -vcodec h264_nvenc -pix_fmt cuda -preset lossless -filter_hw_device 0 -vf hwupload,yadif_cuda=1 -acodec copy -r 60 -f mp4 output.mp4
 
