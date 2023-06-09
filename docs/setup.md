# Setup

## Running on Your Machine

To run on your machine, first create an environment by running

```
conda create --name NAME --file=requirements.txt anaconda
```

Everything is configured so that you can simply run

```
python3 engine.py
```

to see it in action.

## Overview of Files

### `analysis`

Basic stats about data generated by the engine to discuss in the results section.

### `data`

Folder for data. Note that the subfolders `data/boxes` and `data/images` are reserved for intermediate output. It's recommended that videos are placed in `data/videos`.

### `docs`

You're here right now.

### `exploration`

Deprecated python notebooks used for prototyping the final models and scripts. The file structure has changed a few times, so some edits may be needed to make notebooks functional.

### `output`

Recommended folder to store output.

### `(root folder)`

- `classify.py` - Script that, after pre-processing, performs feature extraction and solicits input from the user to label the result data.
- `engine.py` - The Engine running our system. Handles file input and progress monitoring.
- `preprocess.py` - Performs initial OCR to detect and merge high-probability bounding boxes for text.
- `process.py` - Once groups are classified, performs the work of extracting the actual sentences and formatting in a friendly way in the output.
- `vid2frames.py` Simple `ffmpeg` wrapper that converts a video to frames at a given rate.
