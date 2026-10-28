# Anime GAN Studio

A small Streamlit web app for running the supplied `generator.h5` Keras GAN model.

## Run on Windows

1. Install Python 3.10 or 3.11 (64-bit) if needed.
2. Extract this ZIP file to a folder.
3. Open Command Prompt in that folder.
4. Create and activate a virtual environment:

   ```bat
   py -3.11 -m venv .venv
   .venv\Scripts\activate
   ```

5. Install dependencies:

   ```bat
   python -m pip install --upgrade pip
   pip install -r requirements.txt
   ```

6. Start the app:

   ```bat
   streamlit run app.py
   ```

7. Open the local URL Streamlit prints (usually http://localhost:8501) in your browser.

## Run on macOS/Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
streamlit run app.py
```

## Notes

- `generator.h5` is the supplied trained model; training is not required to generate images.
- The model expects a vector of 100 random values and outputs a 64×64 RGB image.
- Since this is an unconditional GAN, the character name is a label in the UI, not a prompt that changes the image. To make names control the generated character, train a conditional GAN with labels or use a text-conditioned image model.
- If TensorFlow installation fails, use 64-bit Python 3.10/3.11 and install dependencies in a fresh virtual environment.
