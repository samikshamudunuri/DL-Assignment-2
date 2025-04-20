https://colab.research.google.com/drive/1PZnNTZ20a8naeBaUOp9qpjH8Kn4SixIH?usp=sharing:link to colab notebook for transliteration

https://colab.research.google.com/drive/1qVl1L3mQ6vQ794fm-X3en0C9Wg7ScpVd?usp=sharing :link to the colab notebook for lyrics


1)Q)(a) Total number of computations:

Assuming:

Embedding size = m

Hidden state size = k

Sequence length = T

Vocabulary size = V

Encoder (1 layer):
T × (m × k + k × k + k)

Decoder (1 layer):
T × (k × k + k × k + k + k × V)

Total:
T × [(m × k + k × k + k) + (2k × k + k + k × V)]

(b) Total number of parameters:

Embedding layer: V × m

Encoder RNN: m × k + k × k + k

Decoder RNN: k × k + k × k + k

Dense output layer: k × V + V

Total:
(V × m) + (m × k + k × k + k) + (2k × k + k) + (k × V + V)

(c) Accuracy and predictions (example):

Test Accuracy: e.g., 83.5%




2)Q)GPT-2 Song Lyrics Generation
This project fine-tunes a pre-trained GPT-2 model on a dataset of song lyrics from various artists. The goal is to generate new, creative song lyrics based on a given prompt using the fine-tuned model.

Features
Fine-tune GPT-2 on a diverse set of song lyrics.

Generate new song lyrics based on a text prompt.

Customize the generation process with parameters like temperature, top-k sampling, and more.

Dataset
The project uses the Poetry Dataset from Kaggle, which includes song lyrics from various artists across different genres. You can download the dataset using the Kaggle API.

Requirements
To run this project, you'll need the following Python packages:

transformers: For working with the GPT-2 model.

datasets: For loading and processing the song lyrics dataset.

torch: PyTorch for training and inference with the GPT-2 model.

kaggle: For downloading the dataset from Kaggle.

Installation & Setup

Download the Dataset:

Make sure you have the Kaggle API credentials (kaggle.json) in your working directory.

Run the Kaggle API commands to download and unzip the dataset.

Fine-Tune GPT-2:

The pre-trained GPT-2 model is fine-tuned on the song lyrics dataset.

The fine-tuning process involves adjusting the model's weights based on the song lyrics, so it can generate more accurate and relevant lyrics.

Generate Song Lyrics:

After fine-tuning, you can generate new lyrics by providing a starting prompt (e.g., "The sun sets over the horizon").

The model generates song lyrics based on the provided prompt, making it a creative tool for lyric generation.
