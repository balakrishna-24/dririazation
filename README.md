# Audio Diarization with Deepgram

This project demonstrates how to perform speaker diarization on audio content using the Deepgram API. The specific example processes a video of Anderson Cooper experiencing a schizophrenia simulator, showing how to extract audio and analyze speaker segments.

## Features

- Download YouTube videos using yt-dlp
- Extract audio from video files using FFmpeg
- Process audio with Deepgram's speaker diarization API
- Generate timestamped transcripts with speaker labels

## Prerequisites

Before running this code, you'll need:

- Python 3.x
- A Deepgram API key (get one at [Deepgram's website](https://deepgram.com))
- FFmpeg installed on your system

## Required Python Packages

```bash
pip install yt-dlp
pip install deepgram-sdk
pip install requests
```

## Installation

1. Clone this repository:
```bash
git clone [your-repo-url]
cd [your-repo-name]
```

2. Install the required packages:
```bash
pip install -r requirements.txt
```

3. Set up your Deepgram API key:
```python
DEEPGRAM_API_KEY = 'your_api_key'  # Replace with your actual API key
```

## Usage

The project consists of several steps:

1. **Download Video**
```python
youtube_video_url = 'your_youtube_url'
file_path = download_video(youtube_video_url)
```

2. **Extract Audio**
```python
!ffmpeg -i input_video.mp4 -q:a 0 -map a audio_output.wav
```

3. **Process with Deepgram**
```python
# The code will process the audio file and output speaker-diarized transcripts
# See the main script for complete implementation
```

## Output Format

The output will be in the following format:
```
Speaker 0 [1.16s - 12.11s]: Transcript text here...
Speaker 1 [12.75s - 14.76s]: Different speaker's text here...
```

## Features of the Diarization

- Speaker identification
- Timestamp generation
- Punctuation
- Multiple speaker detection
- High accuracy transcription

## API Parameters

The code uses the following Deepgram API parameters:
```python
params = {
    'diarize': 'true',
    'utterances': 'true',
    'punctuate': 'true'
}
```

## Error Handling

The code includes error handling for:
- Failed video downloads
- Audio extraction issues
- API request failures
- Response parsing problems

## Contributing

Feel free to contribute to this project by:
1. Forking the repository
2. Creating your feature branch (`git checkout -b feature/AmazingFeature`)
3. Committing your changes (`git commit -m 'Add some AmazingFeature'`)
4. Pushing to the branch (`git push origin feature/AmazingFeature`)
5. Opening a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Deepgram for providing the speech-to-text API
- yt-dlp for YouTube video downloading capabilities
- FFmpeg for audio processing

## Disclaimer

This code is for educational purposes and demonstrates the use of a schizophrenia simulator video. It should be used responsibly and with consideration for those affected by mental health conditions.
