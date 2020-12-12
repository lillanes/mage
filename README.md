Mage
====

Send locally stored videos to your Smart TV or other UPnP/DLNA media renderer.
This is intended as the simplest approach for sending a video through the local
network.

Mage works by setting up a temporary HTTP server that hosts only the video
file, and sending its URI to the rendering device via UPnP protocols.

## Setup

This is a Python 3 application. It uses
[Twisted](https://pypi.org/project/Twisted/) and
[requests](https://pypi.org/project/requests/). For your convenience you can
set everything up in a virtual environment as follows:

```sh
python -m venv venv
source venv/bin/activate
python -m pip install -r requirements.txt
```

## Usage

Pass the video file as argument, and Mage casts to the first media renderer
found on the network:

```sh
./mage.py /path/to/video.mp4
```

## Acknowledgements

This implementation borrows a lot from the
[video2smarttv](https://github.com/probonopd/video2smarttv) project by
[probonopd](https://github.com/probonopd), which in turn uses
[dankrause's](https://github.com/dankrause) solution for [SSDP
discovery](https://gist.github.com/dankrause/6000248). Thanks go to all
developers involved!

