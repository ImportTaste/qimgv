__mpv__

`git-fbcf2bf` from https://sourceforge.net/projects/mpv-player-windows/files/

__opencv__

```
git clone --depth 1 --branch 4.5.5 https://github.com/opencv/opencv.git
cd opencv
cmake -S ./ -B build -G Ninja \
    -DCMAKE_INSTALL_PREFIX="$OPENCV_DIR" \
    -DCMAKE_BUILD_TYPE=Release \
    -DBUILD_LIST='core,imgproc' \
    -DWITH_1394=OFF \
    -DWITH_VTK=OFF \
    -DWITH_FFMPEG=OFF \
    -DWITH_GSTREAMER=OFF \
    -DWITH_DSHOW=OFF \
    -DWITH_QUIRC=OFF \
    -DBUILD_SHARED_LIBS=ON
ninja install -C build
```
