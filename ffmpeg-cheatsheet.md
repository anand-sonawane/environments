# FFMPEG cheatsheet:

### Get specific audio track from a video file

    ffmpeg -i video_name -map 0:a:audio_track_number output_wav_filename

### Cut Audio clips into parts

    ffmpeg -ss start_time -t  duration -i original_audio_name output_wav_filename

### Change video resolution

    ffmpeg -i input_file_name -vf scale=640:360 output_file_name -hide_banner
  
### Change audio sample rate  

    ffmpeg -i input_file_name -ar 44100(new_sample_rate) output_file_name
  
    
### Get video duration in seconds

```python
def get_duration(filename):
    # valid for any audio file accepted by ffprobe
    args = ("ffprobe", "-show_entries", "format=duration", "-i", filename)
    popen = subprocess.Popen(args, stdout=subprocess.PIPE, stderr=subprocess.PIPE)
    output, err = popen.communicate()
    match = re.search(r"[-+]?\d*\.\d+|\d+", output)
    return float(match.group())
```

