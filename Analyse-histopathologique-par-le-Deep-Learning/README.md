# Analyse histopathologique des maladies hépatiques par le Deep Learning

![GitHub](https://img.shields.io/github/license/issam-kebiri/UniversityProjects?color=g&style=for-the-badge)
![GitHub last commit](https://img.shields.io/github/last-commit/issam-kebiri/UniversityProjects?color=red&style=for-the-badge)
![GitHub contributors](https://img.shields.io/github/contributors/issam-kebiri/UniversityProjects?color=yellow&style=for-the-badge)

![GitHub dev_language](https://img.shields.io/badge/Python-yellow?style=flat&logo=python&logoColor=white)
![GitHub dev_language](<https://img.shields.io/badge/Numpy-777BB4?style=flat&logo=numpy&logoColor=white>)
![GitHub dev_language](<https://img.shields.io/badge/Keras-D00000?style=flat&logo=Keras&logoColor=white>)
![GitHub dev_language](<https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=TensorFlow&logoColor=white>)

![GitHub Org's stars](https://img.shields.io/github/stars/issam-kebiri?style=social)
![GitHub followers](https://img.shields.io/github/followers/issam-kebiri?style=social)

## About The Project
Notre travail de recherche présente une étude de segmentation d’images histopathologiques des hépatites du foie en s’inspirant des nouvelles approches et études dans le domaine d’apprentissage profond.

Deux architectures de réseaux de neurones convolutifs sont appliqués pour segmenter une base de données constitué de trois classes de maladies hépatiques. La première architecture est un UNet avec des hyperparamètres personnalisé puis une hybridation de ce modèle avec l’architecture InceptionResNetV2. Nos tests ont d’abords permis d'obtenir un taux de précision de segmentation encouragent de 91,62% avec le modèle UNet personnalisé qu’on a pu faire progresser avec le modèle hybridé InceptionResNetV2-UNet atteignant un résultats remarquable de 96,92%.

### Keywords:
Machin Learning, Deep Learning, convolutional neural networks, liver diseases, histopathological images, transfer Learning, UNet, InceptionResNetV2-UNet.

### Built With

* Python 3.9
* TensorFlow 2.5
* Keras 2.2

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install :

```bash
pip install tensorflow 
pip install keras
pip install visualkeras
```

## Packages
```python
import os
import sys
import random
import numpy as np
import cv2
import matplotlib.pyplot as plt

import tensorflow as tf
import visualkeras
from tensorflow import keras
from tensorflow.keras import layers
from tensorflow.keras.preprocessing.image import ImageDataGenerator
from tensorflow.keras.layers import Conv2D, BatchNormalization, Activation, MaxPool2D, Conv2DTranspose, Concatenate, Input, ZeroPadding2D
from tensorflow.keras.models import Model
from tensorflow.keras.applications import InceptionResNetV2

print("TensorFlow version: ", tf.__version__)
```


## Dataset 

Histopathlogique_liver_&_colon Data_set :
* 1471 images histopathologiques + masks.
* 80% foie & 20% colon.
* Hôpital St.Mary, Londres, Royaume-Uni.
* Méthodes d’acquisitions :
  * Scanners de lames Black-X sans coloration H&E.
  * Micro-vecteurs de tissus avec coloration H&E.
* source : www.kaggle.com/dataset/



01.Segmentation_Cancer

* test_set = 4
* validation_set = 39 images
* training_set = 198 images
* totale = 242 images



02.Segmentation_Stéatose

* validation_set = 35 images
* training_set = 400 images
* totale = 435 images


03.Histopathlogique_liver_&_colon

* validation_set = 65 images
* training_set = 670 images 
* totale = 735 images


#### Totale

2909 images



## Architecture
  Unet architecture


<img src="UNet Architecture.png" />




\
UNet customized 

<img src="Architecture UNet personalisé.png" />




## Approach
Notre approche proposée se caractérise par une implémentation d’un réseau de neurone convolutif entièrement connecté (FCN) basé sur l’architecture de UNet avec des hyperparamètres personnalisés puis une hybridation de notre modèle UNet personnalisé avec une architecture populaire appelé Inception-ResNetV2 utilisées sur trois ensembles de données qu’on a combinées en introduisant des poids pré-entrainés par le bais du Transfer Learning (fine tuning précisément) ce qui boostera nos résultats.
L’organigramme de notre approche proposée est illustré ci-dessous :

<img src="Mon approche.png" />


## Result
<img src="Résultats\R InceptionResNetV2-UNet Perte.png" />
<img src="Résultats\R InceptionResNetV2-UNet précision.png" />
<img src="Résultats\Résultats 01.png" />
<img src="Résultats\Resultats 02.png" />
<img src="Résultats\Resultats 03.png" />
<img src="Résultats\Resultats 04.png" />
<img src="Résultats\Résultats 05.png" />



## License

[GPL-3.0](https://choosealicense.com/licenses/gpl-3.0/)

## Contact

📫 How to reach me: issam.eddine.kebiri@gmail.com

🌐 My Portfolio: <https://issam-kebiri.github.io/>

🔗 Project Link: [https://github.com/issam-kebiri/UniversityProjects/tree/main/Analyse-histopathologique-par-le-Deep-Learning](https://github.com/issam-kebiri/UniversityProjects/tree/main/Analyse-histopathologique-par-le-Deep-Learning)
