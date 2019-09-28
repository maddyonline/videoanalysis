# Setup
```sh
conda create --name va-2 --file spec-file.txt
conda activate va-2
pip install -r myreqs.txt
```

Verify the following command works.

Download file
```sh
youtube-dl -f 'bestvideo[ext=mp4]+bestaudio[ext=m4a]/best[ext=mp4]/best' -o '%(id)s.%(ext)s' https://youtu.be/h-aMY8fuFA0
mv h-aMY8fuFA0.mp4 videos/video.mp4
```

```sh
./getModels.sh
python video.py --path ../../video.mp4 --json true
```

Start `facebox` and then start `videoanalysis` golang applications.

```sh
git clone https://github.com/maddyonline/facebox.git
cd facebox
go get ./...
go build .
mkdir unversioned
./facebox
```

```sh
go build .
mkdir -p unversioned/server-images
./videoanalysis -videos ../../
```


# Acknowledgements

Check out the blog post https://blog.machinebox.io/processing-video-to-do-face-recognition-with-go-and-python-298275a26095 for the original source code.



