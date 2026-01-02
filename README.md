# HAA500: Human-Centric Atomic Action Dataset with Curated Videos

[![Paper](https://img.shields.io/badge/Paper-arXiv-red)](https://arxiv.org/abs/2009.05224)
[![Dataset](https://img.shields.io/badge/Dataset-HAA500%20v1.1-green)](https://drive.google.com/file/d/1nCAiaz6yBMX69YR6ldoVXqlTr2WjGdHM/view?usp=sharing)

Jihoon Chung, Cheng-hsin Wuu, Hsuan-ru Yang, Yu-Wing Tai, Chi-Keung Tang  

![](doc/teaser.png)


## Overview

HAA500 is a manually annotated human-centric atomic action dataset for action recognition on **500 classes** with over **591k labeled frames**. Unlike existing atomic action datasets, where coarse-grained atomic actions were labeled with action-verbs (e.g., "Throw"), HAA500 contains **fine-grained atomic actions** where only consistent actions fall under the same label (e.g., "Baseball Pitching" vs "Free Throw in Basketball"), to minimize ambiguities in action classification.
The dataset has been carefully curated to capture the movement of human figures with less spatio-temporal label noises to greatly enhance the training of deep neural networks.

## Dataset Statistics

- **Classes:** 500 fine-grained atomic action classes
- **Labeled Frames:** 591,000+
- **Format:** YouTube video segments with temporal annotations

## Dataset Format

The dataset consists of 500 text files (one per class), where each file contains video annotations in the following format:

```
youtube_url,start_time,end_time,is_camera_moving,num_of_dominant_figure
```

### Field Descriptions
- `youtube_url`: YouTube video URL
- `start_time`: Start time of the action segment (in seconds)
- `end_time`: End time of the action segment (in seconds)
- `is_camera_moving`: Binary flag (0 or 1) indicating if the camera is moving
- `num_of_dominant_figure`: Number of dominant human figures in the video

### Data Split
- **Training set:** First 16 lines of each class file
- **Validation set:** 17th line of each class file
- **Test set:** Remaining lines


### Example (pushup.txt):
```
https://www.youtube.com/watch?v=IODxDxX7oi4,3.37,7.08,1,1
https://www.youtube.com/watch?v=AhdtowFDKT0,182.71,185.11,0,1
https://www.youtube.com/watch?v=cABuP6ZdUno,7.18,8.58,0,1
...
```

## Download

**HAA500 v1.1 (Latest Version)**  
[Google Drive (raw, video)](https://drive.google.com/file/d/1nCAiaz6yBMX69YR6ldoVXqlTr2WjGdHM/view?usp=sharing)  
[Google Drive (frames)](https://drive.google.com/file/d/1MHaD3_suKrgq87nMbHjwYYWD2m8l2UGS/view?usp=sharing)


**HAA500 v1.0 (Used in Paper)**  
[Google Drive](https://drive.google.com/file/d/1dNGMHbKQ7RnTf2L2TWFLn9qKQ4u5dGek/view?usp=sharing)

## BibTeX
```bibtex
@inproceedings{haa500,
    title={HAA500: Human-Centric Atomic Action Dataset with Curated Videos},
    author={Jihoon Chung and Cheng-hsin Wuu and Hsuan-ru Yang and Yu-Wing Tai and Chi-Keung Tang},
    booktitle = {ICCV 2021}
}
```
## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

