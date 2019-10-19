# video2gif

## prerequisite

please install [**ffmpeg**](https://ffmpeg.org/) first.

e.g. on macOS with Homebrew:

```bash
brew install ffmpeg
```

## install

download [**video2gif.sh**](https://github.com/an63/video2gif/blob/master/video2gif.sh), `chmod +x video2gif.sh`, and enjoy it!

## usage

```text
video2gif: convert video into high quality animated gif with ffmpeg
  - version 1.0.0 @ 2019.10.19
  - https://github.com/an63/video2gif

Usage:
    video2gif.sh [options] input_file

Default:
    Cut 5-second clip from middle of the input file, generate custom palette,
    convert into GIF at 10 fps and its width & height won't exceed 720px.

Options:
    -a: position to start cutting (default: middle of the input)
    -d: duration of the clip in seconds (default: 5)
    -n: no cutting (override -a -d)
    -f: frames per second (default: 10)
    -s: optimize for static background
    -t: speed up / slow down (default is x1.0)
    -r: rotate in clockwise, e.g. 90, 180 (default is 0)
    -w: width of resizing (default is -1 to keep the aspect ratio)
    -h: height of resizing (default is -1 to keep the aspect ratio)
    -l: max of width & height (default is 720, overridden by -w -h)
    -c: save the clip after converting
    -v: display & save the verbose ffmpeg logs
    -o: output job_name (default is timestamp under 'output' folder)

Examples:
    $ video2gif.sh -a 1 -d 8 -r 90 -v input.wmv
    $ video2gif.sh -a 00:12:34 -d 10 -s input.mp4
    $ video2gif.sh -n -f 15 -t 2 -l 320 input.mov
```
