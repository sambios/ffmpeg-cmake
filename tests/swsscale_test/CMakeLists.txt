cmake_minimum_required(VERSION 3.2)

link_directories(/home/yuan/lab/ffmpeg-dev/prebuilt/lib)
include_directories(/home/yuan/lab/ffmpeg-dev/ffmpeg-4.1-cmake)
add_executable(sws_yuv2rgb_test sws_yuv2rgb.cpp)
target_link_libraries(sws_yuv2rgb_test
        avdevice
        avfilter
        postproc
        avformat
        avcodec
        swresample
        swscale
        avutil
        pthread)