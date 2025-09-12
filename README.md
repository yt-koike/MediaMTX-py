# MediaMTX-py

This is an unofficial Python wrapper for [MediaMTX](https://mediamtx.org/)

# How to use

1. Clone this repository
2. execute `pip install .` in the cloned directory.

After installation, you can use MediaMTX like as follows.

```
from mediamtx import MediaMTX
mtx = MediaMTX()
yaml = mtx.get_yaml() # Get mediamtx.yml
yaml["paths"][name] = {"source": url}
mtx.set_yaml(yaml) # Set mediamtx.yml
mtx.start() # Start MediaMTX on another thread
mtx.stop() # Stop the MediaMTX on the thread
```
