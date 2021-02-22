Just I don't want to install [FFmpeg](https://ffmpeg.org/) on my local machine.

# How to use
1. clone this repository & put your movie file in `origin` folder

2. update env about video file names

CAUTION: Overwrite an exist video file if same `AFTER_PROCESSING_FILE` name is exists.

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    env:
      BEFORE_PROCESSING_FILE: shortcut-to-github1s.mov
      AFTER_PROCESSING_FILE: shortcut-to-github1s.gif
```

3. update FFmpeg options if you need

```yaml
      - name: Execute ffmpeg
        run: ffmpeg -y -i origin/${{ env.BEFORE_PROCESSING_FILE }} -vf scale=800:-1 -r 10 processed/${{ env.AFTER_PROCESSING_FILE }}
```

4. commit & push

5. GitHub Actions bot commit a processed video file into `processed` folder

## Author
[Katsuhisa Kitano](https://twitter.com/katsuhisa__)