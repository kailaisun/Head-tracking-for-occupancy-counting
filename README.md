# Occupancy-counting



## Environment
- The code is tested on Ubuntu 20.04.2, python 3.8, cuda 11.1.
- The code is tested on Windows 10, python 3.8, cuda 11.1.


## Installation

Please refer to [Installation]((https://github.com/PaddlePaddle/PaddleDetection/blob/release/2.6/docs/tutorials/INSTALL_cn.md) for installation instructions for Paddle and PaddleDet. It is recommanded to install PaddleDet with pip3.

 1. Clone this repository
  ```bash
  git clone https://github.com/kailaisun/Head-tracking-for-occupancy-counting
  ```

2. Replace all files
   e.g., replace infer_cfg_pphuman.yml in the deploy\pipeline\config.
   replace cfg_utils.py in the deploy\pipeline.
   add pipeline_3.py in the deploy\pipeline.

3. Download trained  [models](https://cloud.tsinghua.edu.cn/d/c12f31ff76294990b654/)
   replace the deploy\pipeline\models folder.


## Dataset Example
Our dataset is not open source due to privacy. But we can show some samples with mosaic below:
![Image 1](outdoor_example.png) | ![Image 2](indoor_example.png) | ![Image 3](side_example.png)

## Test 

A short example video is uploaded, you can test our method with the following order. You can also infer other videos by change the video_file root.

```Bash
python deploy/pipeline/pipeline_3.py --config deploy/pipeline/config/infer_cfg_pphuman.yml --video_file example.mp4 --device gpu --do_entrance_counting --draw_center_traj --child True
```

The infer result of example video is shown below:

![Demo GIF](output.gif)

