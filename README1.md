# Audio Sentiment Analysis
This repository contains code for performing sentiment analysis on call center audio recordings. Follow the steps below to set up and run the analysis:

## Steps:

1. **Install Miniconda**:
    - Begin by installing Miniconda, a lightweight version of Anaconda. You can download it from the official website.

2. **Create a New Environment**:
    - Open a terminal or command prompt and create a new environment using the following command:
      ```
      conda create -p ./env/sent-anal python=3.6
      ```

3. **Activate the Environment**:
    - Activate the newly created environment using the following command:
      ```
      conda activate D:\\ai\\test\\github\\Audio-Sentiment-Analysis\\env\\sent-anal
      ```

4. **Install Required Packages**:
    - Install the necessary Python packages by running:
      ```
      pip install -r requirements.txt
      ```

5. **Prepare Audio Data**:
    - Place your call center audio recordings in the `input` folder.
    - Rename the audio file you want to analyze to \"test.wav\".

6. **Speaker Diarization**:
    - Run the `speaker_diarization.py` script to perform speaker diarization on the call center audio:
      ```
      python ./speaker_diarization.py ./input/test.wav
      ```

7. **Sentiment Classification**:
    - Finally, execute the `run_model.py` script to run sentiment analysis on the processed audio data.
    - You can customize the input file folder within the `run_model.py` script.

## Files:

- **sentiment_classification**:
  - This file is responsible for creating the sentiment analysis model.

- **speaker_diarization**:
  - This file handles the speaker diarization process for call center calls:
    - Label 0: Call center representative
    - Label 1: Customer

- **run_model**:
  - Use this file to run the trained sentiment analysis model on your data.
