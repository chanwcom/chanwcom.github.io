 ---
 title: ""
 categories:
   - Tutorials
 tags:
   - minimal mistakes
   - jekyll
   - blog
   - standard
 toc: true
 toc_sticky: true
 toc_label: "GITHUB BLOG START"
 toc_icon: "blog"
 ---

# Introduction



1. You may download the data from the following website.
https://www.kaggle.com/datasets/myqrizzo/tf-tutorial-ptb-dataset Using the Sentence
Piece, perform “unigram tokenization" with total number of 1024 tokens. You
may find information about sentence piece in the following website.
https://github.com/google/sentencepiece
You need to obtain model and vocab files.
2. Construct a data pipeline which reads the PTB training set performing unigram tokenization
using SentencePiece. One way to implement this is using tf.data.TextLineDataset
API. In the data pipeline, the original data (xt) needs to be processed to generate
a sequence of a pair of (xt, xt+1).
3. Write the model either using PyTorch and Keras. (You may need to choose one of
them). Both for LSTM and Transformer, the model dimension is 256. The number of
layers will be 3. For Transformers, use 4 heads. Build the decoder structure models.
Also report the total number of parameters in your model. You may need to turn
in the model file as well.
4. Perform training to predict xt+1 given xt. The Adam optimizer with the default
learning rate (1.0e-3) may be a good starting point. You may increase the learning
rate from the default value if training is stil stable. When the model is sufficiently
trained, the inverse square root decay, linear decay, or exponential decay may improve
the performance.
5. Measure the average preplexity on the test set. Perplexity can be calculated by
performing exponentiation to the sequence cross entropy between the ground truth
and the predicted values from the model.

You may need to turn in the followings:
• Vocab file obtained from SentencePiece
• PyTorch or Keras model Python file
• A short report comparing the perplexities using the LSTM and Transformer model.
Also describe what kinds of learning rate scheduling scheme you used.
• Training and evaluation scripts that you used for training the model and obtaining
the perplexity.

