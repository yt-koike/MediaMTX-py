# MediaMTX-py

This is an unofficial Python wrapper for [MediaMTX](https://mediamtx.org/)

# How to use

Execute `pip install git+https://github.com/yt-koike/MediaMTX-py`(Recommended) or `pip install mediamtx-py` to install this package.

After installation, you can use MediaMTX like as follows.

```
from mediamtx import MediaMTX
mtx = MediaMTX() # In __init__(), the MediaMTX binary will be downloaded
yaml = mtx.get_yaml() # Get mediamtx.yml
yaml["paths"][name] = {"source": url}
mtx.set_yaml(yaml) # Set mediamtx.yml
mtx.start() # Start MediaMTX on another thread
mtx.stop() # Stop the MediaMTX on the thread
```
