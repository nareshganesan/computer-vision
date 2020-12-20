# Computer vision projects

Applications built using computer vision / deep learning algorithms.

## Udacity projects

| Task        |             Name             |
| ----------- | :--------------------------: |
| [Project 1] | [Facial keypoints detection] |

## Object detection projects

| Task               |            Name             |
| ------------------ | :-------------------------: |
| [object-detection] | [object detection projects] |

[//]: # "Udacity projects"
[project 1]: https://github.com/nareshganesan/computer-vision/tree/main/udacity-nd/P1_facial_keypoints
[facial keypoints detection]: https://github.com/nareshganesan/computer-vision/tree/main/udacity-nd/P1_facial_keypoints
[//]: # "Object detection projects"
[object-detection]: https://github.com/nareshganesan/computer-vision/tree/main/object-detection
[object detection projects]: https://github.com/nareshganesan/computer-vision/tree/main/object-detection

### development setup

```bash
# give docker group access to x server for display
xhost local:docker

# create docker with necessary dependencies
docker build -t aicvlab -f Dockerfile .

# run the docker with host display access
docker run --runtime=nvidia --rm \
 -p 8888:8888 \
 -e DISPLAY=\$DISPLAY \
 -v /tmp/.X11-unix/:/tmp/.X11-unix \
 -v `pwd`:/src \
 nareshganesan/aicvlab:latest /bin/bash
```
