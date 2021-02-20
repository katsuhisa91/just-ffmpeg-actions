Just I don't want to install [FFmpeg](https://ffmpeg.org/) on my local machine.

# How to use
1. clone this repository

2. update env about video file names

CAUTION: Overwrite an exist video file if same `AFTER_PROCESSING_FILE` name is exists.

```yaml
name: Create Archive
on: push
jobs:
  build:
    runs-on: ubuntu-latest
    env:
      BEFORE_PROCESSING_FILE: shortcut-to-github1s.mov
      AFTER_PROCESSING_FILE: shortcut-to-github1s.gif
```

3. commit & push

4. GitHub Actions bot commit a processed video file into `processed` folder

## Author
[Katsuhisa Kitano](https://twitter.com/katsuhisa__)