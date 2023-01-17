---
tile: Helper one-liners
---

Here are some useful one-liners, you can put these in your shell aliases or scripts:

quickly access your note files with grep, rofi, xargs and micro 

```
ls -p ~/Notes/ | grep -v / | rofi -dmenu | xargs -I {} micro ~/Notes/{}
```

show ascii representations

```
man ascii | grep -m 1 -A 63 --color=never Oct
```

convert youtube channels and users into RSS in your [newsboat](https://newsboat.org/) subscription list

```
sed -i "s/channel\//feeds\/videos.xml\?channel_id=/g" $HOME/.newsboat/urls ; sed -i "s/user\//feeds\/videos.xml\?user=/g" $HOME/.newsboat/urls
```

put tree of files into html

```
tree -H '.' -L 1 --noreport --charset utf-8 > index.html
```

burn iso or img image of your Linux distribution

```
sudo dd if=./image.img of=/dev/sdh bs=4M status=progress && sync
```

use a virtual Python environment

```
python3 -m venv env && source env/bin/activate
```

trim with ffmpeg from 00:01:00.000 to the end of a file

```
ffmpeg -i input.mp3 -ss 00:01:00.000 -acodec copy output.mp3
```

trim with ffmpeg from 00:01:00.000 for 5 minutes

```
ffmpeg -i input.mp3 -ss 00:01:00.000 -t 300 -acodec copy output.mp3
```

convert json to yaml with python

```
python3 -c 'import json, sys, yaml ; y=yaml.safe_load(sys.stdin.read()) ; print(json.dumps(y))'
```
