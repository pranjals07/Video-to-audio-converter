# Video to Audio Converter

This project demonstrates how to extract audio from a video file using the `moviepy` library in Python. It allows users to convert video files into audio files with just a few lines of code.

---

## Prerequisites

### Install MoviePy
To use this project, ensure the `moviepy` library is installed. Run the following command in your terminal or command prompt:
```bash
pip install moviepy
```

### Verify Installation
To verify that the library is installed, use the following command:
```bash
pip show moviepy
```

---

## How to Use

1. **Prepare Your Video File**
   - Place the video file (e.g., `song.mp4`) in the same directory as your Python script.

2. **Write the Script**
   Use the following Python code to extract audio from the video file:
   ```python
   from moviepy.editor import VideoFileClip

   # Define the input video file and output audio file
   mp4_file = "song.mp4"
   mp3_file = "audio.mp3"

   # Load the video clip
   video_clip = VideoFileClip(mp4_file)

   # Extract the audio from the video clip
   audio_clip = video_clip.audio

   # Write the audio to a separate file
   audio_clip.write_audiofile(mp3_file)

   # Close the video and audio clips
   audio_clip.close()
   video_clip.close()

   print("Audio extraction successful!")
   ```

3. **Run the Script**
   Execute the script in your Python environment. The audio file (e.g., `audio.mp3`) will be generated in the same directory.

---

## Features

- Extracts audio from any video file supported by MoviePy.
- Saves the extracted audio as an `.mp3` file for easy use.

---

## Example

If your video file is named `song.mp4`, running the script will create an audio file named `audio.mp3` in the same folder. The output message will confirm the extraction:
```text
Audio extraction successful!
```


