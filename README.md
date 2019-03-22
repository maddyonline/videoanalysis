# Setup
```sh
conda create --name va-2 --file spec-file.txt
conda activate va-2
pip install -r myreqs.txt
```

Verify the following command works.

```sh
python video.py --path unversioned/videos/arm-swing-youtube.mpg
```

Start `facebox` and then start `videoanalysis` golang applications.

```sh
./videoanalysis -videos unversioned/videos
```


# Acknowledgements

Check out the blog post https://blog.machinebox.io/processing-video-to-do-face-recognition-with-go-and-python-298275a26095 for the original source code.



