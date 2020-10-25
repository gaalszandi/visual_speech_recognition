# Deep Learning Homework
### IMG17 Visual Speech Recognition

There are a lot of studies considering speech recognition from visual and audio sources. Our application is useful for creating subtitles automatic for videos, where the mouth can be seen.

Our goal is to process different videos, and find out what word was spelled. In our dataset we have different words and for each word we have around 1000 videos.

**1. milestone**
*Data processing*

* data_processing.ipynb

The script for processing the data. We advise you to run the script in Google Colaboratory. The script pull this repository and unzip the data_processing.zip.
If you would like to run the script in another environment you have to check the file pathes in the script and install packages listed in requirements.txt. Besides this you have to install 'ffmpeg' package with the command:
``` sudo apt install ffmpeg ```

* requirements.txt

It contains the necessary packages to install.

* data_processing.zip

It contains example input data for the data processing script and the predictor .dat model for mouth detection. After running the script in colab the results are generated in the ./example/output directory.
