# Bot-Detection-Mouse-Telemetry

A smart, scalable, and ultra-lightweight proof-of-concept that detects bots using only mouse telemetry and 4 simple math operations — no need for server-side deep learning.

Project Overview

This system distinguishes between human and bot users based on their natural mouse movements. Unlike heavy ML models that run on the server, we perform most computations in the browser and only send 2 latent values to the backend.
What It Does

    Tracks mouse telemetry (x, y, dt) in the browser.
    Runs a compressed model in JavaScript using ONNX.
    Sends latent vector [x1, x2] to Flask backend.
    Backend uses 4 simple math operations to predict: human or bot.
    Sets a cookie based on result — updates view accordingly.

How to Run
Step 1: Install Dependencies

pip install -r requirements.txt

Step 2: Run the Flask Server
Option A: With PyTorch model

python app.py


Step 3: Open in Browser

Visit: http://127.0.0.1:5000

Move your mouse around — if your movements are natural, you’ll be redirected to a human-only page (human.html)!
Requirements Summary

    Python ≥ 3.8
    Flask
    For ML version: PyTorch
    For analysis: Jupyter, pandas, matplotlib, torch, etc. (see requirements.txt)
