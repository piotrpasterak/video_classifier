# Image and Video Classifier Project

W ponizszym projekcie zaimplementowałem pierwszą wersje mechanizmu rozpoznawania obrazu.
Jest ona pierwsza ponieważ planuję rozwijac i ulepszac tę implementacje.

Mechanizm ten oparty jest o framework TensorFlow który jest odpowiedzialny za implementacje sieci neuronowej.
Jako model został przyjety wczesniej przygotowany ("nauczony") model o nazwie mask_rcnn_inception_resnet_v2_atrous_coco_2018_01_28.
Model ten uzyskałem dzieki bibliotece COCO API (https://github.com/cocodataset/cocoapi).

wiecej informacji o tego typu modelu można uzyskać tutaj (https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/instance_segmentation.md)
## Zależności
Do pracy implementacja wymaga:
* TensorFlow (https://www.tensorflow.org/) w wersji 2.0
* Biblioteki Keras (https://keras.io/) 
* Interpretatora jezyka python 3.6

## Użycie
Projekt podzielony jest na dwa skrypty w jezyku Python:
* image_classifier.py - jest skryptem rozpoznawania obrazów ulokowanych w katalogu models/research/object_detection/test_images.
* video_classifier.py - jest skryptem rozpoznawania video strumieniowanego z web kamery.

aby użyc któregokolwiek ze skrytów wystrczy go uruchomić z lini poleceń bez parametrów. 

## Wyniki
Osiągnięte wyniki sa zadowalajace ale nie idealne: 
![Result](Recognize.png "Recognized frame")

W kilku rzadkich przypadkach obiekty nie były właściwie rozpoznawane co wynika ze słabości samego modelu.
W tej wersji implementacji model o wiekszych możliwosciach nie mógł być wykorzystany z powodu braku wsparcia dla obliczen na GPU przy użyciu technologii CUDA.
