## How to Run

### Step 1: Prepare a Video

Place the input video in the corresponding working directory.

Example:

```text
input_video.mp4
```

---

### Step 2: Extract Keyframes

Go to the emotion recognition module:

```bash
cd Gpt_Emotion_Recognition/movement
python pipeline.py your_video_name
```

Then save the extracted keyframes:

```bash
python save.py your_video_name
```

---

### Step 3: Recognize Video Emotion

Run the GPT-based emotion recognition script:

```bash
python Callgpt.py
```

The output should be an emotion description or a group of emotion keywords, such as:

```text
peaceful, warm, nostalgic
```

---

### Step 4: Generate Music Prompt

Convert the emotion recognition result into a music generation prompt.

Example:

```text
Generate a warm and nostalgic background music with soft piano, gentle strings, slow tempo, and cinematic atmosphere.
```

---

### Step 5: Generate Background Music

Use the music generation module:

```bash
cd audiocraft
python test_musicgen.py
```

Or run the customized mixing script:

```bash
python mix_bark_musicgen.py
```

The generated music will be saved as an audio file, such as:

```text
output.wav
```

---

## Example Output

Input:

```text
A short video showing a quiet sunset, slow camera movement, and a lonely character.
```

Emotion recognition result:

```text
lonely, calm, nostalgic
```

Generated music prompt:

```text
A calm and nostalgic cinematic background music, slow tempo, soft piano, light strings, emotional and peaceful atmosphere.
```

Output:

```text
Generated background music: output.wav
```
