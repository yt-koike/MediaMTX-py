# MediaMTX-py

This is an unofficial Python wrapper for [MediaMTX](https://mediamtx.org/)

# How to use

Execute `pip install git+https://github.com/yt-koike/MediaMTX-py`(Recommended) or `pip install mediamtx-py` to install this package.

After installation, you can use MediaMTX like as follows.

```
from mediamtx import MediaMTX
mtx = MediaMTX("amd64") # In __init__(), the MediaMTX binary will be downloaded
yaml = mtx.get_yaml() # Get mediamtx.yml
yaml["paths"][name] = {"source": url}
mtx.set_yaml(yaml) # Set mediamtx.yml
mtx.start() # Start MediaMTX on another thread
mtx.stop() # Stop the MediaMTX on the thread
```

MediaMTX() takes four arguments: arch, platform, version and overwrite.

- arch = Architecture: basically "amd64" or "arm64".
- platform = Platform OS: basically "linux", "windows" or "darwin". (Default: value of platform.system().lower())
- version = If set to "latest", it will download the latest MediaMTX. You also can specify the version like "v1.15.3" (Default: "latest")
- overwrite = If set to False, it will preserve the downloaded MediaMTX. (Default: True)
