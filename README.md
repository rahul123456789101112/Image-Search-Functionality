# Simple Image Search Engine


## Overview
- Simple image-based image search engine using Keras + Flask. You can launch the search engine just by running two python scripts.
- `offline.py`: This script extracts a deep-feature from each database image. Each feature is a 4096D fc6 activation from a VGG16 model with ImageNet pre-trained weights.
- `server.py`: This script runs a web-server. You can send your query image to the server via a Flask web-interface. The server finds similar images to the query by a simple linear scan.



## Links
- [Demo](https://www.simple-image-search.xyz/)
- [Course at CVPR2020](https://matsui528.github.io/cvpr2020_tutorial_retrieval/) [[slides](https://speakerdeck.com/matsui_528/cvpr20-tutorial-live-coding-demo-to-implement-an-image-search-engine-from-scratch)] [[video](https://www.youtube.com/watch?v=M0Y9_vBmYXU)]
- [Project page](http://yusukematsui.me/project/sis/sis.html)
- [Tutorial](https://ourcodeworld.com/articles/read/981/how-to-implement-an-image-search-engine-using-keras-tensorflow-with-python-3-in-ubuntu-18-04) and [Video](https://www.youtube.com/watch?v=Htu7b8PUyRg) by [@sdkcarlos](https://github.com/sdkcarlos)

## Usage
```bash
pip install -r requirements.txt

# Put your image files (*.jpg) on static/img

# Then fc6 features are extracted and saved on static/feature
# Note that it takes time for the first time because Keras downloads the VGG weights.
python offline.py

# Now you can do the search via localhost:5000
python server.py
```

