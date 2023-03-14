 Dataset:

https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_Dataset.zip
https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_text.


EXAMPLES

![68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f313630302f312a3642464f496453486c6b32345a33444645616b766e512e706e67](https://user-images.githubusercontent.com/92212914/224806284-e2d5dc94-c9e9-4af2-81d6-be671b608425.png)
Procedure to Train Model

Clone the repository to preserve directory structure.

git clone https://github.com/akshita79/Image_Caption_Generator.git

Put the required dataset files in train_val_data folder (files mentioned in readme there).

Review config.py for paths and other configurations (explained below).

Run train_val.py.
 
 
 Procedure to Test on new images

Clone the repository to preserve directory structure.

git clone https://github.com/akshita79/Image_Caption_Generator.git

Train the model to generate required files in model_data folder (steps given above).

Put the test images in test_data folder.

Review config.py for paths and other configurations (explained below).

Run test.py.



Configurations (config.py)


config

images_path :- Folder path containing flickr dataset images

train_data_path :- .txt file path containing images ids for training

val_data_path :- .txt file path containing imgage ids for validation

captions_path :- .txt file path containing captions

tokenizer_path :- path for saving tokenizer

model_data_path :- path for saving files related to model

model_load_path :- path for loading trained model

num_of_epochs :- Number of epochs

max_length :- Maximum length of captions. This is set manually after training of model and required for test.py

batch_size :- Batch size for training (larger will consume more GPU & CPU memory)

beam_search_k :- BEAM search parameter which tells the algorithm how many words to consider at a time.

test_data_path :- Folder path containing images for testing/inference

model_type :- CNN Model type to use -> inceptionv3 or vgg16

random_seed :- Random seed for reproducibility of results


rnnConfig

embedding_size :- Embedding size used in Decoder(RNN) Model

LSTM_units :- Number of LSTM units in Decoder(RNN) Model

dense_units :- Number of Dense units in Decoder(RNN) Model

dropout :- Dropout probability used in Dropout layer in Decoder(RNN) Model

