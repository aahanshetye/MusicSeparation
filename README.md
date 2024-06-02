# MusicSeparation

This repository demonstrates how to separate music tracks into vocals and accompaniment using [Spleeter](https://github.com/deezer/spleeter), a pre-trained source separation model by Deezer. <br>
The examples use Python and are designed to be run in a Jupyter Notebook environment.

## Getting Started

### Prerequisites

Ensure you have the following installed:
- [FFmpeg](https://ffmpeg.org/)
- [Spleeter](https://github.com/deezer/spleeter)

### Installation

1. Install FFmpeg:

    ```bash
    !apt install ffmpeg
    ```

2. Install Spleeter:

    ```bash
    !pip install spleeter
    ```

### Usage

1. **Download and Play a Music File**

    Download a music file from the repository and play it using IPython's Audio display:

    ```python
    from IPython.display import Audio

    # Download the music file
    !wget https://raw.githubusercontent.com/aahanshetye/MusicSeparation/main/KillerQueen.mp3

    # Play the music file
    Audio('KillerQueen.mp3')
    ```

2. **Separate Music Sources**

    Use Spleeter to separate the music file into vocals and accompaniment:

    ```python
    # Separate the music file
    !spleeter separate KillerQueen.mp3 -o output

    # List the separated files
    !ls output/KillerQueen

    # Play the separated files
    Audio('output/KillerQueen/vocals.wav')
    Audio('output/KillerQueen/accompaniment.wav')
    ```

3. **Repeat for Another Song**

    You can repeat the process for another song:

    ```python
    # Download another music file
    !wget https://raw.githubusercontent.com/aahanshetye/MusicSeparation/main/BangBang.mp3

    # Play the music file
    Audio('BangBang.mp3')

    # Separate the music file
    !spleeter separate BangBang.mp3 -o output

    # List the separated files
    !ls output/BangBang

    # Play the separated files
    Audio('output/BangBang/vocals.wav')
    Audio('output/BangBang/accompaniment.wav')
    ```

## Examples:

### Killer Queen by Queen

Original:

```python
Audio('KillerQueen.mp3')
```

Separated Vocals:

```python
Audio('output/KillerQueen/vocals.wav')
```

Separated Accompaniment:

```python
Audio('output/KillerQueen/accompaniment.wav')
```

### Bang Bang by Vishal-Shekhar, Benny Dayal and Neeti
Original:

```python
Audio('BangBang.mp3')
```

Separated Vocals:

```python
Audio('output/BangBang/vocals.wav')
```

Separated Accompaniment:

```python
Audio('output/BangBang/accompaniment.wav')
```
