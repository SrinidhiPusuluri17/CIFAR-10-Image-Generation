Image Captioning using VGG16 + LSTM
This project performs automatic image captioning using a hybrid model combining VGG16 (as an encoder CNN) and LSTM (as a decoder RNN). The model takes an image as input and generates a natural language description.

📌 Overview
Image captioning is a challenging task that combines computer vision and natural language processing. The model here consists of:

Encoder: A pre-trained VGG16 CNN used to extract visual features from images.

Decoder: A custom LSTM-based RNN to generate natural language captions from the image features.

The process can be divided into two logical stages:

Visual Feature Extraction – using VGG16 without the final classification layer.

Caption Generation – using an LSTM that takes in encoded features and generates a sentence.

🧠 Dataset
Dataset Used: Flickr8k

Contains 8,092 images with five captions each.

Train/Test split: 4,098 for training, remainder for testing/validation.

Alternatives: Flickr30k and MS-COCO (recommended for better performance but require more resources).

Note: Due to limited computational resources, Flickr8k was used for training in this implementation.

📊 Evaluation Metric
BLEU Score (Bilingual Evaluation Understudy) is used to evaluate the similarity between predicted and actual captions.

BLEU scores range from 0 to 1, with values closer to 1 indicating more accurate captions.

Evaluation is implemented using nltk.translate.bleu_score.

🧪 Results
✅ Good Captions:
Images where the model predicted captions with high BLEU scores.

