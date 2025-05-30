# dddmr_documentation_materials
Use following command to convert mp4 to gif
```
ffmpeg -i open_file.mp4 -filter_complex "[0:v] fps=12,scale=1280:-1,split [a][b];[a] palettegen [p];[b][p] paletteuse" open_file.gif
```
Use following command to increase mp4 speed by 2X
```
ffmpeg -i input.mp4 -vf "setpts=0.5*PTS" output.mp4
```
Scale down the gif
```
ffmpeg -i input.gif -vf "scale=iw/2:ih/2" output.gif
```
