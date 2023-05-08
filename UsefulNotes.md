# Useful Notes

If the whisper version is not the least, you can use the following command to convert the audio for better quality:
```shell
ffmpeg -i input.mp3 -ar 16000 -ac 1 -c:a pcm_s16le output.wav
```

Run the command
```shell
python -m whisperx *.wav --model medium --diarize --language en --hf_token [hf_token] --min_speakers 3 --max_speakers 6
```

If you are not sudoer, you can use the following command to install the package:
```shell
conda install ffmpeg

# OSError('sndfile library not found') OSError: sndfile library not found
conda install librosa

# ImportError: /usr/lib/aarch64-linux-gnu/libstdc++.so.6: version `GLIBCXX_3.x.xx' not found
conda install gcc=12.1.0
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$HOME/miniconda3/env/YOUR_ENV_NAME/lib
```
