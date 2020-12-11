# Deep Learning Homework
### IMG17 Visual Speech Recognition

Csapatnév: Disapproving Corgis

Csapattagok:

* Nyárády Dorottya
* Gaál Alexandra
* Berdó Dániel

There are a lot of studies considering speech recognition from visual and audio sources. Our application is useful for creating subtitles automatic for videos, where the mouth can be seen.

Our goal is to process different videos, and find out what word was spelled. In our dataset we have different words and for each word we have around 1000 videos.

**1. milestone** ---------------------------------------------------------------------

*Data processing*

* data_processing.ipynb

The script for processing the data. We advise you to run the script in Google Colaboratory. The script pull this repository and unzip the data_processing.zip.

If you would like to run the script in another environment you have to check the file pathes in the script and install packages listed in requirements.txt. Besides this you have to install 'ffmpeg' package with the command:
``` sudo apt install ffmpeg ```

* requirements.txt

It contains the necessary packages to install.

* data_processing.zip

It contains example input data for the data processing script and the predictor .dat model for mouth detection. After running the script in colab the results are generated in the ./example/output directory.

**2. milestone** -------------------------------------------------------------------

*Training model*

* training_script.ipynb

In the script we implemented a video frame generator class to read training data from directory during training. This class can use transformations given by an ImageDataGenerator type variable for data augmentation as well.

<ins>ResNet + bidirectional GRU</ins>

The idea of the used model is from the document on the link below:

https://arxiv.org/pdf/1703.04105.pdf

This model consists of a frontend part where they use **Conv3D** layers with pooling and batch normalization to extract low-level features from the sequences of the video frames (grayscale images). After that a **ResNet** architecture is used to get higher level features. (It uses 2D convolution) The backend of the network consists of bidirectional **GRU or LSTM** layers. At the end a Dense layer is used with softmax activation for classification. The model can be used with temporal convulation instead of memory cells.

The result experiences can be seen after the training cell!

The model is tested on the test set from LRW dataset. The confusion matrix and the detailed results can be seen.

We advise you to run the script in Google Colaboratory. 
(The script uses a dataset10.zip file which is not included in the repository because  to use the LRW dataset you need to ask permission from the owner. We did that and we got it but it is not permitted to share the content with anyone.)

* tb_logs.zip

It contains the training results in tensorboard logs. You can open it with the Run Tensorboard block if you set the correct path.

* trained_models.zip

It contains the best trained model so far.

* label.txt

It contains the labels of the trained models in order.
