# Setup

1. Install Library:
``` bash
sudo apt-get update
sudo apt-get install libxcb-xinerama0
sudo apt-get install libxrender1 libxi6
```

2. Set Debug Environment Variable (Optional):
``` bash
export QT_DEBUG_PLUGINS=1
```

# Example

- create venv
``` bash
python3 -m venv .venv
source .venv/bin/activate
```

- install library
``` bash
pip install opencv-python
```

- create main.py
``` bash
nano main.py
```
``` python
from random import randint
import numpy as np
import cv2

while True:
    img = np.full([500,500,3], [randint(0,255), randint(0,255), randint(0,255)], dtype=np.uint8)
    cv2.imshow('img', img)
    cv2.waitKey(500)
```
``` bash
python3 main.py
```

- `ctrl + c` for exit
