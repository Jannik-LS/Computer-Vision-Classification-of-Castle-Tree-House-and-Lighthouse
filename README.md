```python
!pip install fiftyone scikit-learn matplotlib seaborn
```

    Requirement already satisfied: fiftyone in /usr/local/lib/python3.11/dist-packages (1.4.1)
    Requirement already satisfied: scikit-learn in /usr/local/lib/python3.11/dist-packages (1.6.1)
    Requirement already satisfied: matplotlib in /usr/local/lib/python3.11/dist-packages (3.10.1)
    Requirement already satisfied: seaborn in /usr/local/lib/python3.11/dist-packages (0.13.2)
    Requirement already satisfied: aiofiles in /usr/local/lib/python3.11/dist-packages (from fiftyone) (24.1.0)
    Requirement already satisfied: argcomplete in /usr/local/lib/python3.11/dist-packages (from fiftyone) (3.6.2)
    Requirement already satisfied: beautifulsoup4 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (4.13.4)
    Requirement already satisfied: boto3 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (1.37.36)
    Requirement already satisfied: cachetools in /usr/local/lib/python3.11/dist-packages (from fiftyone) (5.3.1)
    Requirement already satisfied: dacite<1.8.0,>=1.6.0 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (1.7.0)
    Requirement already satisfied: Deprecated in /usr/local/lib/python3.11/dist-packages (from fiftyone) (1.2.18)
    Requirement already satisfied: ftfy in /usr/local/lib/python3.11/dist-packages (from fiftyone) (6.3.1)
    Requirement already satisfied: humanize in /usr/local/lib/python3.11/dist-packages (from fiftyone) (4.12.2)
    Requirement already satisfied: hypercorn>=0.13.2 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (0.17.3)
    Requirement already satisfied: Jinja2>=3 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (3.1.6)
    Requirement already satisfied: kaleido!=0.2.1.post1 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (0.2.1)
    Requirement already satisfied: mongoengine~=0.29.1 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (0.29.1)
    Requirement already satisfied: motor~=3.6.0 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (3.6.1)
    Requirement already satisfied: numpy in /usr/local/lib/python3.11/dist-packages (from fiftyone) (1.26.0)
    Requirement already satisfied: packaging in /usr/local/lib/python3.11/dist-packages (from fiftyone) (23.1)
    Requirement already satisfied: pandas in /usr/local/lib/python3.11/dist-packages (from fiftyone) (2.2.3)
    Requirement already satisfied: Pillow>=6.2 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (11.2.1)
    Requirement already satisfied: plotly>=4.14 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (6.0.1)
    Requirement already satisfied: pprintpp in /usr/local/lib/python3.11/dist-packages (from fiftyone) (0.4.0)
    Requirement already satisfied: psutil in /usr/local/lib/python3.11/dist-packages (from fiftyone) (7.0.0)
    Requirement already satisfied: pymongo~=4.9.2 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (4.9.2)
    Requirement already satisfied: pytz in /usr/local/lib/python3.11/dist-packages (from fiftyone) (2025.2)
    Requirement already satisfied: PyYAML in /usr/local/lib/python3.11/dist-packages (from fiftyone) (6.0.2)
    Requirement already satisfied: regex in /usr/local/lib/python3.11/dist-packages (from fiftyone) (2024.11.6)
    Requirement already satisfied: retrying in /usr/local/lib/python3.11/dist-packages (from fiftyone) (1.3.4)
    Requirement already satisfied: rtree in /usr/local/lib/python3.11/dist-packages (from fiftyone) (1.4.0)
    Requirement already satisfied: scikit-image in /usr/local/lib/python3.11/dist-packages (from fiftyone) (0.25.2)
    Requirement already satisfied: scipy in /usr/local/lib/python3.11/dist-packages (from fiftyone) (1.15.2)
    Requirement already satisfied: setuptools in /usr/local/lib/python3.11/dist-packages (from fiftyone) (68.2.2)
    Requirement already satisfied: sseclient-py<2,>=1.7.2 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (1.8.0)
    Requirement already satisfied: sse-starlette<1,>=0.10.3 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (0.10.3)
    Requirement already satisfied: starlette>=0.24.0 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (0.46.2)
    Requirement already satisfied: strawberry-graphql in /usr/local/lib/python3.11/dist-packages (from fiftyone) (0.265.1)
    Requirement already satisfied: tabulate in /usr/local/lib/python3.11/dist-packages (from fiftyone) (0.9.0)
    Requirement already satisfied: xmltodict in /usr/local/lib/python3.11/dist-packages (from fiftyone) (0.14.2)
    Requirement already satisfied: universal-analytics-python3<2,>=1.0.1 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (1.1.1)
    Requirement already satisfied: pydash in /usr/local/lib/python3.11/dist-packages (from fiftyone) (8.0.5)
    Requirement already satisfied: fiftyone-brain<0.21,>=0.20.1 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (0.20.1)
    Requirement already satisfied: fiftyone-db<2.0,>=0.4 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (1.1.7)
    Requirement already satisfied: voxel51-eta<0.15,>=0.14.0 in /usr/local/lib/python3.11/dist-packages (from fiftyone) (0.14.0)
    Requirement already satisfied: opencv-python-headless in /usr/local/lib/python3.11/dist-packages (from fiftyone) (4.11.0.86)
    Requirement already satisfied: joblib>=1.2.0 in /usr/local/lib/python3.11/dist-packages (from scikit-learn) (1.4.2)
    Requirement already satisfied: threadpoolctl>=3.1.0 in /usr/local/lib/python3.11/dist-packages (from scikit-learn) (3.6.0)
    Requirement already satisfied: contourpy>=1.0.1 in /usr/local/lib/python3.11/dist-packages (from matplotlib) (1.3.2)
    Requirement already satisfied: cycler>=0.10 in /usr/local/lib/python3.11/dist-packages (from matplotlib) (0.12.1)
    Requirement already satisfied: fonttools>=4.22.0 in /usr/local/lib/python3.11/dist-packages (from matplotlib) (4.57.0)
    Requirement already satisfied: kiwisolver>=1.3.1 in /usr/local/lib/python3.11/dist-packages (from matplotlib) (1.4.8)
    Requirement already satisfied: pyparsing>=2.3.1 in /usr/lib/python3/dist-packages (from matplotlib) (2.4.7)
    Requirement already satisfied: python-dateutil>=2.7 in /usr/local/lib/python3.11/dist-packages (from matplotlib) (2.9.0.post0)
    Requirement already satisfied: h11 in /usr/local/lib/python3.11/dist-packages (from hypercorn>=0.13.2->fiftyone) (0.14.0)
    Requirement already satisfied: h2>=3.1.0 in /usr/local/lib/python3.11/dist-packages (from hypercorn>=0.13.2->fiftyone) (4.2.0)
    Requirement already satisfied: priority in /usr/local/lib/python3.11/dist-packages (from hypercorn>=0.13.2->fiftyone) (2.0.0)
    Requirement already satisfied: wsproto>=0.14.0 in /usr/local/lib/python3.11/dist-packages (from hypercorn>=0.13.2->fiftyone) (1.2.0)
    Requirement already satisfied: MarkupSafe>=2.0 in /usr/local/lib/python3.11/dist-packages (from Jinja2>=3->fiftyone) (2.1.3)
    Requirement already satisfied: tzdata>=2022.7 in /usr/local/lib/python3.11/dist-packages (from pandas->fiftyone) (2025.2)
    Requirement already satisfied: narwhals>=1.15.1 in /usr/local/lib/python3.11/dist-packages (from plotly>=4.14->fiftyone) (1.35.0)
    Requirement already satisfied: dnspython<3.0.0,>=1.16.0 in /usr/local/lib/python3.11/dist-packages (from pymongo~=4.9.2->fiftyone) (2.7.0)
    Requirement already satisfied: six>=1.5 in /usr/lib/python3/dist-packages (from python-dateutil>=2.7->matplotlib) (1.16.0)
    Requirement already satisfied: anyio<5,>=3.6.2 in /usr/local/lib/python3.11/dist-packages (from starlette>=0.24.0->fiftyone) (4.9.0)
    Requirement already satisfied: httpx>=0.10.0 in /usr/local/lib/python3.11/dist-packages (from universal-analytics-python3<2,>=1.0.1->fiftyone) (0.28.1)
    Requirement already satisfied: dill in /usr/local/lib/python3.11/dist-packages (from voxel51-eta<0.15,>=0.14.0->fiftyone) (0.4.0)
    Requirement already satisfied: future in /usr/local/lib/python3.11/dist-packages (from voxel51-eta<0.15,>=0.14.0->fiftyone) (1.0.0)
    Requirement already satisfied: glob2 in /usr/local/lib/python3.11/dist-packages (from voxel51-eta<0.15,>=0.14.0->fiftyone) (0.7)
    Requirement already satisfied: jsonlines in /usr/local/lib/python3.11/dist-packages (from voxel51-eta<0.15,>=0.14.0->fiftyone) (4.0.0)
    Requirement already satisfied: py7zr in /usr/local/lib/python3.11/dist-packages (from voxel51-eta<0.15,>=0.14.0->fiftyone) (0.22.0)
    Requirement already satisfied: rarfile in /usr/local/lib/python3.11/dist-packages (from voxel51-eta<0.15,>=0.14.0->fiftyone) (4.2)
    Requirement already satisfied: requests in /usr/local/lib/python3.11/dist-packages (from voxel51-eta<0.15,>=0.14.0->fiftyone) (2.31.0)
    Requirement already satisfied: sortedcontainers in /usr/local/lib/python3.11/dist-packages (from voxel51-eta<0.15,>=0.14.0->fiftyone) (2.4.0)
    Requirement already satisfied: tzlocal in /usr/local/lib/python3.11/dist-packages (from voxel51-eta<0.15,>=0.14.0->fiftyone) (5.3.1)
    Requirement already satisfied: urllib3 in /usr/local/lib/python3.11/dist-packages (from voxel51-eta<0.15,>=0.14.0->fiftyone) (2.0.5)
    Requirement already satisfied: soupsieve>1.2 in /usr/local/lib/python3.11/dist-packages (from beautifulsoup4->fiftyone) (2.6)
    Requirement already satisfied: typing-extensions>=4.0.0 in /usr/local/lib/python3.11/dist-packages (from beautifulsoup4->fiftyone) (4.8.0)
    Requirement already satisfied: botocore<1.38.0,>=1.37.36 in /usr/local/lib/python3.11/dist-packages (from boto3->fiftyone) (1.37.36)
    Requirement already satisfied: jmespath<2.0.0,>=0.7.1 in /usr/local/lib/python3.11/dist-packages (from boto3->fiftyone) (1.0.1)
    Requirement already satisfied: s3transfer<0.12.0,>=0.11.0 in /usr/local/lib/python3.11/dist-packages (from boto3->fiftyone) (0.11.5)
    Requirement already satisfied: wrapt<2,>=1.10 in /usr/local/lib/python3.11/dist-packages (from Deprecated->fiftyone) (1.14.1)
    Requirement already satisfied: wcwidth in /usr/local/lib/python3.11/dist-packages (from ftfy->fiftyone) (0.2.13)
    Requirement already satisfied: networkx>=3.0 in /usr/local/lib/python3.11/dist-packages (from scikit-image->fiftyone) (3.4.2)
    Requirement already satisfied: imageio!=2.35.0,>=2.33 in /usr/local/lib/python3.11/dist-packages (from scikit-image->fiftyone) (2.37.0)
    Requirement already satisfied: tifffile>=2022.8.12 in /usr/local/lib/python3.11/dist-packages (from scikit-image->fiftyone) (2025.3.30)
    Requirement already satisfied: lazy-loader>=0.4 in /usr/local/lib/python3.11/dist-packages (from scikit-image->fiftyone) (0.4)
    Requirement already satisfied: graphql-core<3.4.0,>=3.2.0 in /usr/local/lib/python3.11/dist-packages (from strawberry-graphql->fiftyone) (3.2.6)
    Requirement already satisfied: idna>=2.8 in /usr/local/lib/python3.11/dist-packages (from anyio<5,>=3.6.2->starlette>=0.24.0->fiftyone) (3.4)
    Requirement already satisfied: sniffio>=1.1 in /usr/local/lib/python3.11/dist-packages (from anyio<5,>=3.6.2->starlette>=0.24.0->fiftyone) (1.3.1)
    Requirement already satisfied: hyperframe<7,>=6.1 in /usr/local/lib/python3.11/dist-packages (from h2>=3.1.0->hypercorn>=0.13.2->fiftyone) (6.1.0)
    Requirement already satisfied: hpack<5,>=4.1 in /usr/local/lib/python3.11/dist-packages (from h2>=3.1.0->hypercorn>=0.13.2->fiftyone) (4.1.0)
    Requirement already satisfied: certifi in /usr/local/lib/python3.11/dist-packages (from httpx>=0.10.0->universal-analytics-python3<2,>=1.0.1->fiftyone) (2023.7.22)
    Requirement already satisfied: httpcore==1.* in /usr/local/lib/python3.11/dist-packages (from httpx>=0.10.0->universal-analytics-python3<2,>=1.0.1->fiftyone) (1.0.8)
    Requirement already satisfied: attrs>=19.2.0 in /usr/local/lib/python3.11/dist-packages (from jsonlines->voxel51-eta<0.15,>=0.14.0->fiftyone) (25.3.0)
    Requirement already satisfied: texttable in /usr/local/lib/python3.11/dist-packages (from py7zr->voxel51-eta<0.15,>=0.14.0->fiftyone) (1.7.0)
    Requirement already satisfied: pycryptodomex>=3.16.0 in /usr/local/lib/python3.11/dist-packages (from py7zr->voxel51-eta<0.15,>=0.14.0->fiftyone) (3.22.0)
    Requirement already satisfied: pyzstd>=0.15.9 in /usr/local/lib/python3.11/dist-packages (from py7zr->voxel51-eta<0.15,>=0.14.0->fiftyone) (0.16.2)
    Requirement already satisfied: pyppmd<1.2.0,>=1.1.0 in /usr/local/lib/python3.11/dist-packages (from py7zr->voxel51-eta<0.15,>=0.14.0->fiftyone) (1.1.1)
    Requirement already satisfied: pybcj<1.1.0,>=1.0.0 in /usr/local/lib/python3.11/dist-packages (from py7zr->voxel51-eta<0.15,>=0.14.0->fiftyone) (1.0.3)
    Requirement already satisfied: multivolumefile>=0.2.3 in /usr/local/lib/python3.11/dist-packages (from py7zr->voxel51-eta<0.15,>=0.14.0->fiftyone) (0.2.3)
    Requirement already satisfied: inflate64<1.1.0,>=1.0.0 in /usr/local/lib/python3.11/dist-packages (from py7zr->voxel51-eta<0.15,>=0.14.0->fiftyone) (1.0.1)
    Requirement already satisfied: brotli>=1.1.0 in /usr/local/lib/python3.11/dist-packages (from py7zr->voxel51-eta<0.15,>=0.14.0->fiftyone) (1.1.0)
    Requirement already satisfied: charset-normalizer<4,>=2 in /usr/local/lib/python3.11/dist-packages (from requests->voxel51-eta<0.15,>=0.14.0->fiftyone) (3.2.0)
    [33mWARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv[0m[33m
    [0m
    [1m[[0m[34;49mnotice[0m[1;39;49m][0m[39;49m A new release of pip is available: [0m[31;49m23.2.1[0m[39;49m -> [0m[32;49m25.0.1[0m
    [1m[[0m[34;49mnotice[0m[1;39;49m][0m[39;49m To update, run: [0m[32;49mpython3 -m pip install --upgrade pip[0m
    


```python
import os
os.environ['TF_CPP_MIN_LOG_LEVEL'] = '1' # Don't log informations into STDERR, only warnings and errors.
```


```python
import fiftyone as fo
from fiftyone import ViewField as F
import shutil
import random
import sklearn as sk
from sklearn.model_selection import train_test_split
import tensorflow as tf
from tensorflow.keras.preprocessing.image import ImageDataGenerator, img_to_array, array_to_img
from tensorflow.keras.applications import VGG19
from tensorflow.keras.optimizers import Adam
from tensorflow.keras import layers, models, Model
import matplotlib.pyplot as plt
import numpy as np
import seaborn as sns
from sklearn.metrics import confusion_matrix, classification_report
import cv2
import pandas as pd
import PIL
from PIL import Image
from collections import Counter
import hashlib
```

    2025-04-20 11:26:52.375530: E tensorflow/compiler/xla/stream_executor/cuda/cuda_dnn.cc:9342] Unable to register cuDNN factory: Attempting to register factory for plugin cuDNN when one has already been registered
    2025-04-20 11:26:52.375568: E tensorflow/compiler/xla/stream_executor/cuda/cuda_fft.cc:609] Unable to register cuFFT factory: Attempting to register factory for plugin cuFFT when one has already been registered
    2025-04-20 11:26:52.375601: E tensorflow/compiler/xla/stream_executor/cuda/cuda_blas.cc:1518] Unable to register cuBLAS factory: Attempting to register factory for plugin cuBLAS when one has already been registered
    


```python
print("TensorFlow:", tf.__version__)
print("Pandas:", pd.__version__)
print("NumPy:", np.__version__)
print("Scikit-learn:", sk.__version__)
print("OpenCV (cv2):", cv2.__version__)
print("PIL:", PIL.__version__)
print("FiftyOne:", fo.__version__)
```

    TensorFlow: 2.14.0
    Pandas: 2.2.3
    NumPy: 1.26.0
    Scikit-learn: 1.6.1
    OpenCV (cv2): 4.11.0
    PIL: 11.2.1
    FiftyOne: 1.4.1
    


```python
!nvidia-smi
```

    Sun Apr 20 11:26:54 2025       
    +---------------------------------------------------------------------------------------+
    | NVIDIA-SMI 535.216.01             Driver Version: 535.216.01   CUDA Version: 12.2     |
    |-----------------------------------------+----------------------+----------------------+
    | GPU  Name                 Persistence-M | Bus-Id        Disp.A | Volatile Uncorr. ECC |
    | Fan  Temp   Perf          Pwr:Usage/Cap |         Memory-Usage | GPU-Util  Compute M. |
    |                                         |                      |               MIG M. |
    |=========================================+======================+======================|
    |   0  NVIDIA GeForce GTX 1070 Ti     On  | 00000000:29:00.0  On |                  N/A |
    |  0%   53C    P8              12W / 180W |    636MiB /  8192MiB |      0%      Default |
    |                                         |                      |                  N/A |
    +-----------------------------------------+----------------------+----------------------+
                                                                                             
    +---------------------------------------------------------------------------------------+
    | Processes:                                                                            |
    |  GPU   GI   CI        PID   Type   Process name                            GPU Memory |
    |        ID   ID                                                             Usage      |
    |=======================================================================================|
    +---------------------------------------------------------------------------------------+
    

# Data Preparation & Exploration

## Daten herunterladen und exportieren


```python
my_classes = ["Castle", "Tree house", "Lighthouse"]
export_dir = "/content/data"

dataset = fo.zoo.load_zoo_dataset(
    "open-images-v7",
    split="train",
    label_types=["detections"],
    classes=my_classes,
    max_samples=1500,
    shuffle=True
)

dataset = dataset.filter_labels("ground_truth", F("label").is_in(my_classes))
patches = dataset.to_patches("ground_truth")
patches.export(
    export_dir=export_dir,
    dataset_type=fo.types.ImageClassificationDirectoryTree,
    label_field="ground_truth",
)
```

    Downloading split 'train' to '/root/fiftyone/open-images-v7/train' if necessary
    Necessary images already downloaded
    Existing download of split 'train' is sufficient
    Loading 'open-images-v7' split 'train'
     100% |███████████████| 1500/1500 [5.9s elapsed, 0s remaining, 251.3 samples/s]      
    Dataset 'open-images-v7-train-1500' created
    Directory '/content/data' already exists; export will be merged with existing files
    Detected an image classification exporter and a label field 'ground_truth' of type <class 'fiftyone.core.labels.Detection'>. Exporting image patches...
     100% |███████████████| 1691/1691 [20.2s elapsed, 0s remaining, 71.0 samples/s]      
    

## Train/Test Split


```python
def split_dataset(base_dir, output_dir, classes, test_size=0.2):
    train_dir = os.path.join(output_dir, "train")
    test_dir = os.path.join(output_dir, "test")
    os.makedirs(train_dir, exist_ok=True)
    os.makedirs(test_dir, exist_ok=True)

    for cls in classes:
        cls_path = os.path.join(base_dir, cls)
        images = os.listdir(cls_path)
        train_imgs, test_imgs = train_test_split(images, test_size=test_size, random_state=42)
        os.makedirs(os.path.join(train_dir, cls), exist_ok=True)
        os.makedirs(os.path.join(test_dir, cls), exist_ok=True)
        for img in train_imgs:
            shutil.copy(os.path.join(cls_path, img), os.path.join(train_dir, cls, img))
        for img in test_imgs:
            shutil.copy(os.path.join(cls_path, img), os.path.join(test_dir, cls, img))

split_dataset("/content/data", "/content/split_data", my_classes)
```

## ImageDataGenerator vorbereiten


```python
img_size = (224, 224)
batch_size = 32

train_datagen = ImageDataGenerator(rescale=1./255)
test_datagen = ImageDataGenerator(rescale=1./255)

train_generator = train_datagen.flow_from_directory(
    "/content/split_data/train", target_size=img_size, batch_size=batch_size, class_mode='categorical'
)

test_generator = test_datagen.flow_from_directory(
    "/content/split_data/test", target_size=img_size, batch_size=batch_size, class_mode='categorical', shuffle=False
)
```

    Found 1351 images belonging to 3 classes.
    Found 340 images belonging to 3 classes.
    


```python
# Zähle Bilder pro Klasse
class_counts = {}
for cls in my_classes:
    class_dir = os.path.join(export_dir, cls)
    class_counts[cls] = len(os.listdir(class_dir))

# Erstelle DataFrame für Übersicht
df_counts = pd.DataFrame(list(class_counts.items()), columns=["Klasse", "Anzahl"])
df_counts["Prozent"] = 100 * df_counts["Anzahl"] / df_counts["Anzahl"].sum()
df_counts.sort_values("Anzahl", ascending=False, inplace=True)

# Zeige die Tabelle
print(df_counts)

# Visualisierung
plt.figure(figsize=(10,6))
sns.barplot(data=df_counts, x="Klasse", y="Anzahl", palette="pastel")

# Annotiere die Balken mit Anzahl + %
for i, row in df_counts.iterrows():
    plt.text(i, row["Anzahl"] + 5, f'{int(row["Anzahl"])}\n({row["Prozent"]:.1f}%)',
             ha='center', va='bottom', fontsize=10)

plt.title("Klassenverteilung der exportierten Bilder")
plt.xlabel("Klasse")
plt.ylabel("Anzahl der Bilder")
plt.tight_layout()
plt.show()
```

           Klasse  Anzahl    Prozent
    0      Castle    1238  73.211118
    2  Lighthouse     416  24.600828
    1  Tree house      37   2.188054
    

    /tmp/ipykernel_717/2188644875.py:17: FutureWarning: 
    
    Passing `palette` without assigning `hue` is deprecated and will be removed in v0.14.0. Assign the `x` variable to `hue` and set `legend=False` for the same effect.
    
      sns.barplot(data=df_counts, x="Klasse", y="Anzahl", palette="pastel")
    


    
![png](output_12_2.png)
    



```python
image_shapes = []

for cls in my_classes:
    cls_dir = os.path.join(export_dir, cls)
    for img_name in os.listdir(cls_dir):
        img_path = os.path.join(cls_dir, img_name)
        try:
            img = Image.open(img_path)
            image_shapes.append(img.size)  # (width, height)
        except:
            continue

shape_counts = Counter(image_shapes)
df_shapes = pd.DataFrame(shape_counts.items(), columns=["Größe (W, H)", "Anzahl"])
df_shapes.sort_values("Anzahl", ascending=False).head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Größe (W, H)</th>
      <th>Anzahl</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>154</th>
      <td>(1023, 682)</td>
      <td>4</td>
    </tr>
    <tr>
      <th>45</th>
      <td>(1023, 767)</td>
      <td>3</td>
    </tr>
    <tr>
      <th>977</th>
      <td>(110, 133)</td>
      <td>2</td>
    </tr>
    <tr>
      <th>498</th>
      <td>(1023, 723)</td>
      <td>2</td>
    </tr>
    <tr>
      <th>224</th>
      <td>(1023, 681)</td>
      <td>2</td>
    </tr>
    <tr>
      <th>75</th>
      <td>(1022, 1022)</td>
      <td>2</td>
    </tr>
    <tr>
      <th>21</th>
      <td>(393, 335)</td>
      <td>2</td>
    </tr>
    <tr>
      <th>197</th>
      <td>(1023, 562)</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1121</th>
      <td>(155, 67)</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1128</th>
      <td>(904, 504)</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python
mean_colors = []

for cls in my_classes:
    cls_dir = os.path.join(export_dir, cls)
    for img_name in os.listdir(cls_dir)[:50]:  # Nur Sample
        img_path = os.path.join(cls_dir, img_name)
        img = cv2.imread(img_path)
        if img is not None:
            mean_color = cv2.mean(img)[:3]
            mean_colors.append(mean_color)

mean_colors = np.array(mean_colors)

plt.figure(figsize=(12,4))
for i, (color_name, color_code) in enumerate(zip(['Blau', 'Grün', 'Rot'], ['blue', 'green', 'red'])):
    plt.subplot(1, 3, i+1)
    plt.hist(mean_colors[:, i], bins=20, color=color_code, alpha=0.7)
    plt.title(f"Durchschnittlicher {color_name}-Wert")
plt.tight_layout()
plt.show()
```


    
![png](output_14_0.png)
    



```python
def calculate_blurriness(image_path):
    try:
        image = cv2.imread(image_path, cv2.IMREAD_GRAYSCALE)
        return cv2.Laplacian(image, cv2.CV_64F).var()
    except:
        return 0

blur_values = []

for cls in my_classes:
    cls_dir = os.path.join(export_dir, cls)
    for img_name in os.listdir(cls_dir)[:50]:
        img_path = os.path.join(cls_dir, img_name)
        blur_values.append(calculate_blurriness(img_path))

plt.hist(blur_values, bins=30, color="gray")
plt.title("Unschärfe-Index (Laplacian-Varianz)")
plt.xlabel("Schärfe")
plt.ylabel("Anzahl der Bilder")
plt.show()
```


    
![png](output_15_0.png)
    



```python


def file_hash(file_path):
    with open(file_path, 'rb') as f:
        return hashlib.md5(f.read()).hexdigest()

hashes = {}
duplicates = []

for cls in my_classes:
    cls_dir = os.path.join(export_dir, cls)
    for img_name in os.listdir(cls_dir):
        img_path = os.path.join(cls_dir, img_name)
        h = file_hash(img_path)
        if h in hashes:
            duplicates.append((img_path, hashes[h]))
        else:
            hashes[h] = img_path

print(f"{len(duplicates)} mögliche Duplikate gefunden.")
```

    0 mögliche Duplikate gefunden.
    

## Augment & Balance Dataset


```python
# Your original class list and directories
base_split_dir = "/content/split_data"
augmented_dir = "/content/augmented"
img_size = (224, 224)
batch_size = 32

# Augmentation setup
augmentation = ImageDataGenerator(
    rescale=1./255,
    horizontal_flip=True,
    brightness_range=[0.8, 1.2],
    width_shift_range=0.1,
    height_shift_range=0.1,
    fill_mode='nearest'
)

def augment_class_images(source_dir, target_dir, class_name, target_count):
    class_path = os.path.join(source_dir, class_name)
    aug_class_path = os.path.join(target_dir, class_name)
    os.makedirs(aug_class_path, exist_ok=True)

    images = os.listdir(class_path)
    current_count = len(images)

    print(f"Augmenting class '{class_name}': {current_count} -> {target_count}")

    # Copy original images
    for img in images:
        shutil.copy(os.path.join(class_path, img), os.path.join(aug_class_path, img))

    if current_count == 0:
        return  # Avoid division by zero

    i = 0
    while current_count + i < target_count:
        img_name = random.choice(images)
        img_path = os.path.join(class_path, img_name)
        img = Image.open(img_path).convert("RGB").resize(img_size)
        x = img_to_array(img)
        x = np.expand_dims(x, 0)

        for batch in augmentation.flow(x, batch_size=1):
            new_img = array_to_img(batch[0])
            new_img_name = f"aug_{i}_{img_name}"
            new_img.save(os.path.join(aug_class_path, new_img_name))
            i += 1
            if current_count + i >= target_count:
                break
```


```python
# Balance and augment each class
for cls in my_classes:
    source = os.path.join(base_split_dir, "train")
    target = os.path.join(augmented_dir, "train")
    augment_class_images(os.path.join(source), os.path.join(target), cls, 1200)

for cls in my_classes:
    source = os.path.join(base_split_dir, "test")
    target = os.path.join(augmented_dir, "test")
    augment_class_images(os.path.join(source), os.path.join(target), cls, 300)

# Final data generators using augmented data
train_generator_balanced = ImageDataGenerator(rescale=1./255).flow_from_directory(
    os.path.join(augmented_dir, "train"),
    target_size=img_size,
    batch_size=batch_size,
    class_mode='categorical'
)

test_generator_balanced = ImageDataGenerator(rescale=1./255).flow_from_directory(
    os.path.join(augmented_dir, "test"),
    target_size=img_size,
    batch_size=batch_size,
    class_mode='categorical',
    shuffle=False
)
```

    Augmenting class 'Castle': 990 -> 1200
    Augmenting class 'Tree house': 29 -> 1200
    Augmenting class 'Lighthouse': 332 -> 1200
    Augmenting class 'Castle': 248 -> 300
    Augmenting class 'Tree house': 8 -> 300
    Augmenting class 'Lighthouse': 84 -> 300
    Found 3600 images belonging to 3 classes.
    Found 900 images belonging to 3 classes.
    

# Train models

## VGG19 from scratch (unbalanced)


```python
base_vgg19 = VGG19(include_top=False, weights=None, input_shape=(224, 224, 3))
# You can view the layers with model.summary(), 'block5_pool' is the last layer here.
output = base_vgg19.get_layer('block5_pool').output
```


```python
x = layers.Flatten()(output)
x = layers.Dense(512, activation='relu')(x)
x = layers.Dense(3, activation='softmax')(x)
model_scratch = Model(inputs=base_vgg19.input, outputs=x)

# This nests it, which is hard to deal with for Grad-CAM
#model_scratch = models.Sequential([
#    VGG19(include_top=False, weights=None, input_shape=(224, 224, 3)),
#    layers.Flatten(),
#    layers.Dense(512, activation='relu'),
#    layers.Dense(3, activation='softmax')
#])

model_scratch.summary()
```

    Model: "model"
    _________________________________________________________________
     Layer (type)                Output Shape              Param #   
    =================================================================
     input_1 (InputLayer)        [(None, 224, 224, 3)]     0         
                                                                     
     block1_conv1 (Conv2D)       (None, 224, 224, 64)      1792      
                                                                     
     block1_conv2 (Conv2D)       (None, 224, 224, 64)      36928     
                                                                     
     block1_pool (MaxPooling2D)  (None, 112, 112, 64)      0         
                                                                     
     block2_conv1 (Conv2D)       (None, 112, 112, 128)     73856     
                                                                     
     block2_conv2 (Conv2D)       (None, 112, 112, 128)     147584    
                                                                     
     block2_pool (MaxPooling2D)  (None, 56, 56, 128)       0         
                                                                     
     block3_conv1 (Conv2D)       (None, 56, 56, 256)       295168    
                                                                     
     block3_conv2 (Conv2D)       (None, 56, 56, 256)       590080    
                                                                     
     block3_conv3 (Conv2D)       (None, 56, 56, 256)       590080    
                                                                     
     block3_conv4 (Conv2D)       (None, 56, 56, 256)       590080    
                                                                     
     block3_pool (MaxPooling2D)  (None, 28, 28, 256)       0         
                                                                     
     block4_conv1 (Conv2D)       (None, 28, 28, 512)       1180160   
                                                                     
     block4_conv2 (Conv2D)       (None, 28, 28, 512)       2359808   
                                                                     
     block4_conv3 (Conv2D)       (None, 28, 28, 512)       2359808   
                                                                     
     block4_conv4 (Conv2D)       (None, 28, 28, 512)       2359808   
                                                                     
     block4_pool (MaxPooling2D)  (None, 14, 14, 512)       0         
                                                                     
     block5_conv1 (Conv2D)       (None, 14, 14, 512)       2359808   
                                                                     
     block5_conv2 (Conv2D)       (None, 14, 14, 512)       2359808   
                                                                     
     block5_conv3 (Conv2D)       (None, 14, 14, 512)       2359808   
                                                                     
     block5_conv4 (Conv2D)       (None, 14, 14, 512)       2359808   
                                                                     
     block5_pool (MaxPooling2D)  (None, 7, 7, 512)         0         
                                                                     
     flatten (Flatten)           (None, 25088)             0         
                                                                     
     dense (Dense)               (None, 512)               12845568  
                                                                     
     dense_1 (Dense)             (None, 3)                 1539      
                                                                     
    =================================================================
    Total params: 32871491 (125.39 MB)
    Trainable params: 32871491 (125.39 MB)
    Non-trainable params: 0 (0.00 Byte)
    _________________________________________________________________
    


```python
model_scratch.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])
history_scratch = model_scratch.fit(train_generator, epochs=10, validation_data=test_generator)
```

    Epoch 1/10
    43/43 [==============================] - 38s 557ms/step - loss: 0.7454 - accuracy: 0.6973 - val_loss: 0.6737 - val_accuracy: 0.7294
    Epoch 2/10
    43/43 [==============================] - 19s 448ms/step - loss: 0.6751 - accuracy: 0.7328 - val_loss: 0.6675 - val_accuracy: 0.7294
    Epoch 3/10
    43/43 [==============================] - 19s 438ms/step - loss: 0.6653 - accuracy: 0.7328 - val_loss: 0.6996 - val_accuracy: 0.7294
    Epoch 4/10
    43/43 [==============================] - 21s 482ms/step - loss: 0.6702 - accuracy: 0.7328 - val_loss: 0.6754 - val_accuracy: 0.7294
    Epoch 5/10
    43/43 [==============================] - 21s 491ms/step - loss: 0.6620 - accuracy: 0.7328 - val_loss: 0.6717 - val_accuracy: 0.7294
    Epoch 6/10
    43/43 [==============================] - 21s 490ms/step - loss: 0.6622 - accuracy: 0.7328 - val_loss: 0.6928 - val_accuracy: 0.7294
    Epoch 7/10
    43/43 [==============================] - 21s 490ms/step - loss: 0.6605 - accuracy: 0.7328 - val_loss: 0.6708 - val_accuracy: 0.7294
    Epoch 8/10
    43/43 [==============================] - 21s 485ms/step - loss: 0.6642 - accuracy: 0.7328 - val_loss: 0.6726 - val_accuracy: 0.7294
    Epoch 9/10
    43/43 [==============================] - 21s 501ms/step - loss: 0.6600 - accuracy: 0.7328 - val_loss: 0.6644 - val_accuracy: 0.7294
    Epoch 10/10
    43/43 [==============================] - 21s 485ms/step - loss: 0.6656 - accuracy: 0.7328 - val_loss: 0.7010 - val_accuracy: 0.7294
    

## Transfer Learning mit pretrained VGG19 (unbalanced)


```python
base_model = VGG19(include_top=False, weights="imagenet", input_shape=(224, 224, 3))
base_model.trainable = False
# You can view the layers with model.summary(), 'block5_pool' is the last layer here.
output = base_model.get_layer('block5_pool').output
```


```python
x = layers.Flatten()(output)
x = layers.Dense(512, activation='relu')(x)
x = layers.Dense(3, activation='softmax')(x)
model_pretrained = Model(inputs=base_model.input, outputs=x)

# This nests it, which is hard to deal with for Grad-CAM
#model_pretrained = models.Sequential([
#    base_model,
#    layers.Flatten(),
#    layers.Dense(512, activation='relu'),
#    layers.Dense(3, activation='softmax')
#])
model_pretrained.summary()
```

    Model: "model_1"
    _________________________________________________________________
     Layer (type)                Output Shape              Param #   
    =================================================================
     input_2 (InputLayer)        [(None, 224, 224, 3)]     0         
                                                                     
     block1_conv1 (Conv2D)       (None, 224, 224, 64)      1792      
                                                                     
     block1_conv2 (Conv2D)       (None, 224, 224, 64)      36928     
                                                                     
     block1_pool (MaxPooling2D)  (None, 112, 112, 64)      0         
                                                                     
     block2_conv1 (Conv2D)       (None, 112, 112, 128)     73856     
                                                                     
     block2_conv2 (Conv2D)       (None, 112, 112, 128)     147584    
                                                                     
     block2_pool (MaxPooling2D)  (None, 56, 56, 128)       0         
                                                                     
     block3_conv1 (Conv2D)       (None, 56, 56, 256)       295168    
                                                                     
     block3_conv2 (Conv2D)       (None, 56, 56, 256)       590080    
                                                                     
     block3_conv3 (Conv2D)       (None, 56, 56, 256)       590080    
                                                                     
     block3_conv4 (Conv2D)       (None, 56, 56, 256)       590080    
                                                                     
     block3_pool (MaxPooling2D)  (None, 28, 28, 256)       0         
                                                                     
     block4_conv1 (Conv2D)       (None, 28, 28, 512)       1180160   
                                                                     
     block4_conv2 (Conv2D)       (None, 28, 28, 512)       2359808   
                                                                     
     block4_conv3 (Conv2D)       (None, 28, 28, 512)       2359808   
                                                                     
     block4_conv4 (Conv2D)       (None, 28, 28, 512)       2359808   
                                                                     
     block4_pool (MaxPooling2D)  (None, 14, 14, 512)       0         
                                                                     
     block5_conv1 (Conv2D)       (None, 14, 14, 512)       2359808   
                                                                     
     block5_conv2 (Conv2D)       (None, 14, 14, 512)       2359808   
                                                                     
     block5_conv3 (Conv2D)       (None, 14, 14, 512)       2359808   
                                                                     
     block5_conv4 (Conv2D)       (None, 14, 14, 512)       2359808   
                                                                     
     block5_pool (MaxPooling2D)  (None, 7, 7, 512)         0         
                                                                     
     flatten_1 (Flatten)         (None, 25088)             0         
                                                                     
     dense_2 (Dense)             (None, 512)               12845568  
                                                                     
     dense_3 (Dense)             (None, 3)                 1539      
                                                                     
    =================================================================
    Total params: 32871491 (125.39 MB)
    Trainable params: 12847107 (49.01 MB)
    Non-trainable params: 20024384 (76.39 MB)
    _________________________________________________________________
    


```python
model_pretrained.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])
history_pretrained = model_pretrained.fit(train_generator, epochs=10, validation_data=test_generator)
```

    Epoch 1/10
    43/43 [==============================] - 9s 179ms/step - loss: 0.7569 - accuracy: 0.9075 - val_loss: 0.0773 - val_accuracy: 0.9676
    Epoch 2/10
    43/43 [==============================] - 7s 172ms/step - loss: 0.0503 - accuracy: 0.9859 - val_loss: 0.0697 - val_accuracy: 0.9765
    Epoch 3/10
    43/43 [==============================] - 7s 170ms/step - loss: 0.0100 - accuracy: 0.9970 - val_loss: 0.0885 - val_accuracy: 0.9765
    Epoch 4/10
    43/43 [==============================] - 7s 171ms/step - loss: 0.0027 - accuracy: 1.0000 - val_loss: 0.0481 - val_accuracy: 0.9824
    Epoch 5/10
    43/43 [==============================] - 7s 170ms/step - loss: 0.0011 - accuracy: 1.0000 - val_loss: 0.0645 - val_accuracy: 0.9765
    Epoch 6/10
    43/43 [==============================] - 7s 170ms/step - loss: 7.7885e-04 - accuracy: 1.0000 - val_loss: 0.0585 - val_accuracy: 0.9765
    Epoch 7/10
    43/43 [==============================] - 7s 170ms/step - loss: 6.6907e-04 - accuracy: 1.0000 - val_loss: 0.0471 - val_accuracy: 0.9794
    Epoch 8/10
    43/43 [==============================] - 7s 170ms/step - loss: 5.3731e-04 - accuracy: 1.0000 - val_loss: 0.0427 - val_accuracy: 0.9853
    Epoch 9/10
    43/43 [==============================] - 7s 170ms/step - loss: 4.7621e-04 - accuracy: 1.0000 - val_loss: 0.0535 - val_accuracy: 0.9735
    Epoch 10/10
    43/43 [==============================] - 7s 171ms/step - loss: 3.8426e-04 - accuracy: 1.0000 - val_loss: 0.0555 - val_accuracy: 0.9735
    

## VGG19 from Scratch (balanced)


```python
base_vgg19_balanced = VGG19(include_top=False, weights=None, input_shape=(224, 224, 3))

output = base_vgg19_balanced.get_layer('block5_pool').output
x = layers.Flatten()(output)
x = layers.Dense(512, activation='relu')(x)
x = layers.Dense(3, activation='softmax')(x)
model_scratch_balanced = Model(inputs=base_vgg19_balanced.input, outputs=x)

model_scratch_balanced.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])
history_scratch_balanced = model_scratch_balanced.fit(train_generator_balanced, epochs=10, validation_data=test_generator_balanced)
```

    Epoch 1/10
    113/113 [==============================] - 64s 527ms/step - loss: 1.1153 - accuracy: 0.3286 - val_loss: 1.0986 - val_accuracy: 0.3333
    Epoch 2/10
    113/113 [==============================] - 56s 497ms/step - loss: 1.2531 - accuracy: 0.3364 - val_loss: 1.0987 - val_accuracy: 0.3333
    Epoch 3/10
    113/113 [==============================] - 55s 488ms/step - loss: 1.0988 - accuracy: 0.3308 - val_loss: 1.0986 - val_accuracy: 0.3333
    Epoch 4/10
    113/113 [==============================] - 55s 489ms/step - loss: 1.0987 - accuracy: 0.3300 - val_loss: 1.0986 - val_accuracy: 0.3333
    Epoch 5/10
    113/113 [==============================] - 55s 486ms/step - loss: 1.0988 - accuracy: 0.3300 - val_loss: 1.0986 - val_accuracy: 0.3333
    Epoch 6/10
    113/113 [==============================] - 55s 483ms/step - loss: 1.0987 - accuracy: 0.3286 - val_loss: 1.0986 - val_accuracy: 0.3333
    Epoch 7/10
    113/113 [==============================] - 54s 475ms/step - loss: 1.0988 - accuracy: 0.3253 - val_loss: 1.0986 - val_accuracy: 0.3333
    Epoch 8/10
    113/113 [==============================] - 50s 439ms/step - loss: 1.0987 - accuracy: 0.3164 - val_loss: 1.0986 - val_accuracy: 0.3333
    Epoch 9/10
    113/113 [==============================] - 49s 433ms/step - loss: 1.0987 - accuracy: 0.3331 - val_loss: 1.0986 - val_accuracy: 0.3333
    Epoch 10/10
    113/113 [==============================] - 51s 447ms/step - loss: 1.0987 - accuracy: 0.3228 - val_loss: 1.0986 - val_accuracy: 0.3333
    

## Transfer Learning mit pretrained VGG19 (balanced)


```python
base_model_balanced = VGG19(include_top=False, weights="imagenet", input_shape=(224, 224, 3))
base_model_balanced.trainable = False

output = base_model_balanced.get_layer('block5_pool').output
x = layers.Flatten()(output)
x = layers.Dense(512, activation='relu')(x)
x = layers.Dense(3, activation='softmax')(x)
model_pretrained_balanced = Model(inputs=base_model_balanced.input, outputs=x)

model_pretrained_balanced.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])
history_pretrained_balanced = model_pretrained_balanced.fit(train_generator_balanced, epochs=10, validation_data=test_generator_balanced)
```

    Epoch 1/10
    113/113 [==============================] - 18s 153ms/step - loss: 0.3676 - accuracy: 0.9550 - val_loss: 1.3810 - val_accuracy: 0.6844
    Epoch 2/10
    113/113 [==============================] - 17s 152ms/step - loss: 0.0248 - accuracy: 0.9931 - val_loss: 0.6737 - val_accuracy: 0.7389
    Epoch 3/10
    113/113 [==============================] - 17s 150ms/step - loss: 0.0306 - accuracy: 0.9933 - val_loss: 0.5827 - val_accuracy: 0.7778
    Epoch 4/10
    113/113 [==============================] - 17s 150ms/step - loss: 0.0128 - accuracy: 0.9953 - val_loss: 0.0501 - val_accuracy: 0.9889
    Epoch 5/10
    113/113 [==============================] - 17s 150ms/step - loss: 0.0038 - accuracy: 0.9986 - val_loss: 0.1580 - val_accuracy: 0.9567
    Epoch 6/10
    113/113 [==============================] - 19s 165ms/step - loss: 1.2951e-04 - accuracy: 1.0000 - val_loss: 0.0944 - val_accuracy: 0.9667
    Epoch 7/10
    113/113 [==============================] - 17s 151ms/step - loss: 6.4478e-04 - accuracy: 0.9997 - val_loss: 0.1452 - val_accuracy: 0.9478
    Epoch 8/10
    113/113 [==============================] - 17s 151ms/step - loss: 1.0001e-05 - accuracy: 1.0000 - val_loss: 0.1389 - val_accuracy: 0.9478
    Epoch 9/10
    113/113 [==============================] - 17s 153ms/step - loss: 7.3746e-06 - accuracy: 1.0000 - val_loss: 0.1822 - val_accuracy: 0.9278
    Epoch 10/10
    113/113 [==============================] - 17s 154ms/step - loss: 6.4737e-06 - accuracy: 1.0000 - val_loss: 0.1745 - val_accuracy: 0.9300
    

## Experimental Architecture (balanced)


```python
# Load base VGG19 model
base_vgg = VGG19(include_top=False, weights='imagenet', input_shape=(224, 224, 3))

# Freeze layers up to and including block2_conv2
for layer in base_vgg.layers:
    if 'block1_' in layer.name or 'block2_' in layer.name:
        layer.trainable = False
    else:
        layer.trainable = True

# Get output from block4_conv4 (we will stop there)
output_layer_name = 'block4_conv4'
output = base_vgg.get_layer(output_layer_name).output
```


```python
# === Naive Inception Layer ===
# Input shape: (28, 28, 512) for 224x224 input

branch1 = layers.Conv2D(128, kernel_size=1, padding='same', activation=tf.keras.layers.LeakyReLU())(output)
branch2 = layers.Conv2D(128, kernel_size=3, padding='same', activation=tf.keras.layers.LeakyReLU())(output)
branch3 = layers.Conv2D(128, kernel_size=5, padding='same', activation=tf.keras.layers.LeakyReLU())(output)
branch4 = layers.MaxPooling2D(pool_size=3, strides=1, padding='same')(output)
branch4 = layers.Conv2D(128, kernel_size=1, padding='same', activation=tf.keras.layers.LeakyReLU())(branch4)

inception_output = layers.Concatenate()([branch1, branch2, branch3, branch4])  # shape: (28, 28, 512)

# === Additional Conv Layers ===
x = layers.Conv2D(512, kernel_size=3, strides=2, padding='valid', activation='relu')(inception_output)  # output: (13, 13, 512)
x = layers.Conv2D(640, kernel_size=1, strides=1, padding='valid', activation='relu')(x)  # output: (13, 13, 640)

# === Classification Head ===
# x = layers.Flatten(x)
x = layers.GlobalAveragePooling2D()(x)
x = layers.Dense(512, activation='relu')(x)
x = layers.Dense(3, activation='softmax')(x)

# Final model
model_custom = Model(inputs=base_vgg.input, outputs=x)
model_custom.summary()
```

    Model: "model_4"
    __________________________________________________________________________________________________
     Layer (type)                Output Shape                 Param #   Connected to                  
    ==================================================================================================
     input_5 (InputLayer)        [(None, 224, 224, 3)]        0         []                            
                                                                                                      
     block1_conv1 (Conv2D)       (None, 224, 224, 64)         1792      ['input_5[0][0]']             
                                                                                                      
     block1_conv2 (Conv2D)       (None, 224, 224, 64)         36928     ['block1_conv1[0][0]']        
                                                                                                      
     block1_pool (MaxPooling2D)  (None, 112, 112, 64)         0         ['block1_conv2[0][0]']        
                                                                                                      
     block2_conv1 (Conv2D)       (None, 112, 112, 128)        73856     ['block1_pool[0][0]']         
                                                                                                      
     block2_conv2 (Conv2D)       (None, 112, 112, 128)        147584    ['block2_conv1[0][0]']        
                                                                                                      
     block2_pool (MaxPooling2D)  (None, 56, 56, 128)          0         ['block2_conv2[0][0]']        
                                                                                                      
     block3_conv1 (Conv2D)       (None, 56, 56, 256)          295168    ['block2_pool[0][0]']         
                                                                                                      
     block3_conv2 (Conv2D)       (None, 56, 56, 256)          590080    ['block3_conv1[0][0]']        
                                                                                                      
     block3_conv3 (Conv2D)       (None, 56, 56, 256)          590080    ['block3_conv2[0][0]']        
                                                                                                      
     block3_conv4 (Conv2D)       (None, 56, 56, 256)          590080    ['block3_conv3[0][0]']        
                                                                                                      
     block3_pool (MaxPooling2D)  (None, 28, 28, 256)          0         ['block3_conv4[0][0]']        
                                                                                                      
     block4_conv1 (Conv2D)       (None, 28, 28, 512)          1180160   ['block3_pool[0][0]']         
                                                                                                      
     block4_conv2 (Conv2D)       (None, 28, 28, 512)          2359808   ['block4_conv1[0][0]']        
                                                                                                      
     block4_conv3 (Conv2D)       (None, 28, 28, 512)          2359808   ['block4_conv2[0][0]']        
                                                                                                      
     block4_conv4 (Conv2D)       (None, 28, 28, 512)          2359808   ['block4_conv3[0][0]']        
                                                                                                      
     max_pooling2d (MaxPooling2  (None, 28, 28, 512)          0         ['block4_conv4[0][0]']        
     D)                                                                                               
                                                                                                      
     conv2d (Conv2D)             (None, 28, 28, 128)          65664     ['block4_conv4[0][0]']        
                                                                                                      
     conv2d_1 (Conv2D)           (None, 28, 28, 128)          589952    ['block4_conv4[0][0]']        
                                                                                                      
     conv2d_2 (Conv2D)           (None, 28, 28, 128)          1638528   ['block4_conv4[0][0]']        
                                                                                                      
     conv2d_3 (Conv2D)           (None, 28, 28, 128)          65664     ['max_pooling2d[0][0]']       
                                                                                                      
     concatenate (Concatenate)   (None, 28, 28, 512)          0         ['conv2d[0][0]',              
                                                                         'conv2d_1[0][0]',            
                                                                         'conv2d_2[0][0]',            
                                                                         'conv2d_3[0][0]']            
                                                                                                      
     conv2d_4 (Conv2D)           (None, 13, 13, 512)          2359808   ['concatenate[0][0]']         
                                                                                                      
     conv2d_5 (Conv2D)           (None, 13, 13, 640)          328320    ['conv2d_4[0][0]']            
                                                                                                      
     global_average_pooling2d (  (None, 640)                  0         ['conv2d_5[0][0]']            
     GlobalAveragePooling2D)                                                                          
                                                                                                      
     dense_8 (Dense)             (None, 512)                  328192    ['global_average_pooling2d[0][
                                                                        0]']                          
                                                                                                      
     dense_9 (Dense)             (None, 3)                    1539      ['dense_8[0][0]']             
                                                                                                      
    ==================================================================================================
    Total params: 15962819 (60.89 MB)
    Trainable params: 15702659 (59.90 MB)
    Non-trainable params: 260160 (1016.25 KB)
    __________________________________________________________________________________________________
    


```python
# Train
model_custom.compile(optimizer=Adam(learning_rate=1e-4),
                     loss='categorical_crossentropy',
                     metrics=['accuracy'])

#TODO: replace with balanced generators!!
history_custom = model_custom.fit(train_generator_balanced, epochs=10, validation_data=test_generator_balanced)
```

    Epoch 1/10
    113/113 [==============================] - 44s 338ms/step - loss: 0.1810 - accuracy: 0.9331 - val_loss: 0.1242 - val_accuracy: 0.9800
    Epoch 2/10
    113/113 [==============================] - 37s 326ms/step - loss: 0.0819 - accuracy: 0.9694 - val_loss: 0.0888 - val_accuracy: 0.9722
    Epoch 3/10
    113/113 [==============================] - 37s 327ms/step - loss: 0.0614 - accuracy: 0.9761 - val_loss: 0.1055 - val_accuracy: 0.9622
    Epoch 4/10
    113/113 [==============================] - 37s 325ms/step - loss: 0.0430 - accuracy: 0.9828 - val_loss: 0.1255 - val_accuracy: 0.9611
    Epoch 5/10
    113/113 [==============================] - 37s 328ms/step - loss: 0.0465 - accuracy: 0.9853 - val_loss: 0.0406 - val_accuracy: 0.9867
    Epoch 6/10
    113/113 [==============================] - 38s 332ms/step - loss: 0.0624 - accuracy: 0.9783 - val_loss: 0.0407 - val_accuracy: 0.9833
    Epoch 7/10
    113/113 [==============================] - 37s 326ms/step - loss: 0.0305 - accuracy: 0.9881 - val_loss: 0.0472 - val_accuracy: 0.9822
    Epoch 8/10
    113/113 [==============================] - 37s 327ms/step - loss: 0.0755 - accuracy: 0.9742 - val_loss: 0.0325 - val_accuracy: 0.9889
    Epoch 9/10
    113/113 [==============================] - 37s 324ms/step - loss: 0.0276 - accuracy: 0.9897 - val_loss: 0.0575 - val_accuracy: 0.9800
    Epoch 10/10
    113/113 [==============================] - 38s 332ms/step - loss: 0.0229 - accuracy: 0.9917 - val_loss: 0.1407 - val_accuracy: 0.9633
    

# Test models on test-set/ own-images


```python
def get_img_array(img_path, size):
    img = tf.keras.utils.load_img(img_path, target_size=size)
    array = tf.keras.utils.img_to_array(img)
    array = np.expand_dims(array, axis=0)
    array = array / 255.0  # same normalization as during training
    return array, img

def make_gradcam_heatmap(img_array, model, last_conv_layer_name, pred_index=None):
    grad_model = tf.keras.models.Model(
        [model.inputs], [model.get_layer(last_conv_layer_name).output, model.output]
    )

    with tf.GradientTape() as tape:
        conv_outputs, predictions = grad_model(img_array)
        if pred_index is None:
            pred_index = tf.argmax(predictions[0])
        class_channel = predictions[:, pred_index]

    grads = tape.gradient(class_channel, conv_outputs)

    pooled_grads = tf.reduce_mean(grads, axis=(0, 1, 2))

    conv_outputs = conv_outputs[0]
    heatmap = conv_outputs @ pooled_grads[..., tf.newaxis]
    heatmap = tf.squeeze(heatmap)

    heatmap = tf.maximum(heatmap, 0) / tf.math.reduce_max(heatmap)
    return heatmap.numpy()

def display_gradcam(img_path, heatmap, alpha=0.4):
    img = cv2.imread(img_path)
    img = cv2.resize(img, (224, 224))

    heatmap = cv2.resize(heatmap, (img.shape[1], img.shape[0]))
    heatmap_color = cv2.applyColorMap(np.uint8(255 * heatmap), cv2.COLORMAP_JET)

    overlay = heatmap_color * alpha + img
    overlay = np.uint8(overlay)

    plt.figure(figsize=(6, 6))
    plt.imshow(cv2.cvtColor(overlay, cv2.COLOR_BGR2RGB))
    plt.axis('off')
    plt.show()

def plot_history(h1, h2, h3):
    plt.figure(figsize=(12,5))
    plt.subplot(1,2,1)
    plt.plot(h1.history['accuracy'], label="Scratch")
    plt.plot(h2.history['accuracy'], label="Pretrained")
    if h3 is not None:
        plt.plot(h3.history['accuracy'], label="Custom")
    plt.title("Train Accuracy")
    plt.legend()

    plt.subplot(1,2,2)
    plt.plot(h1.history['val_accuracy'], label="Scratch Val")
    plt.plot(h2.history['val_accuracy'], label="Pretrained Val")
    if h3 is not None:
        plt.plot(h3.history['val_accuracy'], label="Custom Val")
    plt.title("Validation Accuracy")
    plt.legend()

    plt.show()
```

Training results on **unbalanced** dataset.

Metrics here are skewed because we don't have enough data to properly validate the performance of these models with such a low dataset.


```python
plot_history(history_scratch, history_pretrained, None)
```


    
![png](output_40_0.png)
    


Training results on **balanced** dataset


```python
plot_history(history_scratch_balanced, history_pretrained_balanced, history_custom)
```


    
![png](output_42_0.png)
    



```python
!unzip -x custom_images.zip
```


```python
# Define image paths
custom_img_paths = {
    "Castle": "./Castle.jpg",
    "Lighthouse": "./Lighthouse.jpg",
    "Tree house": "./Tree House.jpg"
}

# Reverse class index mapping (e.g., {0: 'Castle', 1: 'Lighthouse', 2: 'Tree house'})
class_indices = train_generator_balanced.class_indices
idx_to_class = {v: k for k, v in class_indices.items()}
```

## From Scratch Architecture


```python
Y_pred = model_scratch.predict(test_generator)
y_pred = np.argmax(Y_pred, axis=1)

labels = list(test_generator.class_indices.keys())
cm = confusion_matrix(test_generator.classes, y_pred)

plt.figure(figsize=(8,6))
sns.heatmap(cm, annot=True, fmt="d", xticklabels=labels, yticklabels=labels, cmap="Blues")
plt.xlabel("Predicted")
plt.ylabel("True")
plt.title("Confusion Matrix (unbalanced dataset)")
plt.show()

print(classification_report(test_generator.classes, y_pred, target_names=labels))
```

    11/11 [==============================] - 1s 126ms/step
    


    
![png](output_46_1.png)
    


                  precision    recall  f1-score   support
    
          Castle       0.73      1.00      0.84       248
      Lighthouse       0.00      0.00      0.00        84
      Tree house       0.00      0.00      0.00         8
    
        accuracy                           0.73       340
       macro avg       0.24      0.33      0.28       340
    weighted avg       0.53      0.73      0.62       340
    
    

    /usr/local/lib/python3.11/dist-packages/sklearn/metrics/_classification.py:1565: UndefinedMetricWarning: Precision is ill-defined and being set to 0.0 in labels with no predicted samples. Use `zero_division` parameter to control this behavior.
      _warn_prf(average, modifier, f"{metric.capitalize()} is", len(result))
    /usr/local/lib/python3.11/dist-packages/sklearn/metrics/_classification.py:1565: UndefinedMetricWarning: Precision is ill-defined and being set to 0.0 in labels with no predicted samples. Use `zero_division` parameter to control this behavior.
      _warn_prf(average, modifier, f"{metric.capitalize()} is", len(result))
    /usr/local/lib/python3.11/dist-packages/sklearn/metrics/_classification.py:1565: UndefinedMetricWarning: Precision is ill-defined and being set to 0.0 in labels with no predicted samples. Use `zero_division` parameter to control this behavior.
      _warn_prf(average, modifier, f"{metric.capitalize()} is", len(result))
    


```python
Y_pred = model_scratch_balanced.predict(test_generator_balanced)
y_pred = np.argmax(Y_pred, axis=1)

labels = list(test_generator_balanced.class_indices.keys())
cm = confusion_matrix(test_generator_balanced.classes, y_pred)

plt.figure(figsize=(8,6))
sns.heatmap(cm, annot=True, fmt="d", xticklabels=labels, yticklabels=labels, cmap="Blues")
plt.xlabel("Predicted")
plt.ylabel("True")
plt.title("Confusion Matrix (balanced dataset)")
plt.show()

print(classification_report(test_generator_balanced.classes, y_pred, target_names=labels))
```

    29/29 [==============================] - 3s 113ms/step
    


    
![png](output_47_1.png)
    


                  precision    recall  f1-score   support
    
          Castle       0.00      0.00      0.00       300
      Lighthouse       0.00      0.00      0.00       300
      Tree house       0.33      1.00      0.50       300
    
        accuracy                           0.33       900
       macro avg       0.11      0.33      0.17       900
    weighted avg       0.11      0.33      0.17       900
    
    

    /usr/local/lib/python3.11/dist-packages/sklearn/metrics/_classification.py:1565: UndefinedMetricWarning: Precision is ill-defined and being set to 0.0 in labels with no predicted samples. Use `zero_division` parameter to control this behavior.
      _warn_prf(average, modifier, f"{metric.capitalize()} is", len(result))
    /usr/local/lib/python3.11/dist-packages/sklearn/metrics/_classification.py:1565: UndefinedMetricWarning: Precision is ill-defined and being set to 0.0 in labels with no predicted samples. Use `zero_division` parameter to control this behavior.
      _warn_prf(average, modifier, f"{metric.capitalize()} is", len(result))
    /usr/local/lib/python3.11/dist-packages/sklearn/metrics/_classification.py:1565: UndefinedMetricWarning: Precision is ill-defined and being set to 0.0 in labels with no predicted samples. Use `zero_division` parameter to control this behavior.
      _warn_prf(average, modifier, f"{metric.capitalize()} is", len(result))
    

Grad-CAM for unbalanced model


```python
for label, path in custom_img_paths.items():
    print(f"\n🔍 True label: {label}")

    img_array, _ = get_img_array(path, size=(224, 224))
    preds = model_scratch.predict(img_array)

    pred_class_idx = np.argmax(preds)
    pred_class_name = idx_to_class[pred_class_idx]

    print(f"Predicted class: {pred_class_name} ({preds[0][pred_class_idx]*100:.2f}%)")

    heatmap = make_gradcam_heatmap(img_array, model_scratch, last_conv_layer_name="block5_conv4")
    display_gradcam(path, heatmap)
```

    
    🔍 True label: Castle
    1/1 [==============================] - 0s 21ms/step
    Predicted class: Castle (81.28%)
    


    
![png](output_49_1.png)
    


    
    🔍 True label: Lighthouse
    1/1 [==============================] - 0s 18ms/step
    Predicted class: Castle (81.28%)
    


    
![png](output_49_3.png)
    


    
    🔍 True label: Tree house
    1/1 [==============================] - 0s 17ms/step
    Predicted class: Castle (81.28%)
    


    
![png](output_49_5.png)
    


## Pretrained Architecture


```python
Y_pred = model_pretrained.predict(test_generator)
y_pred = np.argmax(Y_pred, axis=1)

labels = list(test_generator.class_indices.keys())
cm = confusion_matrix(test_generator.classes, y_pred)

plt.figure(figsize=(8,6))
sns.heatmap(cm, annot=True, fmt="d", xticklabels=labels, yticklabels=labels, cmap="Blues")
plt.xlabel("Predicted")
plt.ylabel("True")
plt.title("Confusion Matrix (unbalanced dataset)")
plt.show()

print(classification_report(test_generator.classes, y_pred, target_names=labels))
```

    11/11 [==============================] - 1s 116ms/step
    


    
![png](output_51_1.png)
    


                  precision    recall  f1-score   support
    
          Castle       0.97      1.00      0.98       248
      Lighthouse       0.99      0.95      0.97        84
      Tree house       1.00      0.50      0.67         8
    
        accuracy                           0.97       340
       macro avg       0.99      0.82      0.87       340
    weighted avg       0.97      0.97      0.97       340
    
    


```python
Y_pred = model_pretrained_balanced.predict(test_generator_balanced)
y_pred = np.argmax(Y_pred, axis=1)

labels = list(test_generator_balanced.class_indices.keys())
cm = confusion_matrix(test_generator_balanced.classes, y_pred)

plt.figure(figsize=(8,6))
sns.heatmap(cm, annot=True, fmt="d", xticklabels=labels, yticklabels=labels, cmap="Blues")
plt.xlabel("Predicted")
plt.ylabel("True")
plt.title("Confusion Matrix (balanced dataset)")
plt.show()

print(classification_report(test_generator_balanced.classes, y_pred, target_names=labels))
```

    29/29 [==============================] - 4s 118ms/step
    


    
![png](output_52_1.png)
    


                  precision    recall  f1-score   support
    
          Castle       0.83      1.00      0.90       300
      Lighthouse       1.00      0.99      0.99       300
      Tree house       1.00      0.80      0.89       300
    
        accuracy                           0.93       900
       macro avg       0.94      0.93      0.93       900
    weighted avg       0.94      0.93      0.93       900
    
    

**Grad-CAM unbalanced dataset**


```python
# Predict and visualize
for label, path in custom_img_paths.items():
    print(f"\n🔍 True label: {label}")
    img_array, _ = get_img_array(path, size=(224, 224))

    preds = model_pretrained.predict(img_array)
    pred_class_idx = np.argmax(preds)
    pred_class_name = idx_to_class[pred_class_idx]

    print(f"Predicted class: {pred_class_name} ({preds[0][pred_class_idx]*100:.2f}%)")

    # Generate Grad-CAM
    heatmap = make_gradcam_heatmap(img_array, model_pretrained, last_conv_layer_name="block5_conv4")

    # Show image with heatmap
    display_gradcam(path, heatmap)
```

    
    🔍 True label: Castle
    1/1 [==============================] - 0s 18ms/step
    Predicted class: Castle (100.00%)
    


    
![png](output_54_1.png)
    


    
    🔍 True label: Lighthouse
    1/1 [==============================] - 0s 18ms/step
    Predicted class: Castle (91.17%)
    


    
![png](output_54_3.png)
    


    
    🔍 True label: Tree house
    1/1 [==============================] - 0s 17ms/step
    Predicted class: Castle (97.30%)
    


    
![png](output_54_5.png)
    


**Grad-CAM balanced dataset**


```python
# Predict and visualize
for label, path in custom_img_paths.items():
    print(f"\n🔍 True label: {label}")
    img_array, _ = get_img_array(path, size=(224, 224))

    preds = model_pretrained_balanced.predict(img_array)
    pred_class_idx = np.argmax(preds)
    pred_class_name = idx_to_class[pred_class_idx]

    print(f"Predicted class: {pred_class_name} ({preds[0][pred_class_idx]*100:.2f}%)")

    # Generate Grad-CAM
    heatmap = make_gradcam_heatmap(img_array, model_pretrained_balanced, last_conv_layer_name="block5_conv4")

    # Show image with heatmap
    display_gradcam(path, heatmap)
```

    
    🔍 True label: Castle
    1/1 [==============================] - 0s 24ms/step
    Predicted class: Castle (100.00%)
    


    
![png](output_56_1.png)
    


    
    🔍 True label: Lighthouse
    1/1 [==============================] - 0s 17ms/step
    Predicted class: Lighthouse (99.98%)
    


    
![png](output_56_3.png)
    


    
    🔍 True label: Tree house
    1/1 [==============================] - 0s 18ms/step
    Predicted class: Castle (99.80%)
    


    
![png](output_56_5.png)
    


#### Experimental Architecture

**We only trained on balanced dataset**


```python
Y_pred = model_custom.predict(test_generator_balanced)
y_pred = np.argmax(Y_pred, axis=1)

labels = list(test_generator_balanced.class_indices.keys())
cm = confusion_matrix(test_generator_balanced.classes, y_pred)

plt.figure(figsize=(8,6))
sns.heatmap(cm, annot=True, fmt="d", xticklabels=labels, yticklabels=labels, cmap="Blues")
plt.xlabel("Predicted")
plt.ylabel("True")
plt.title("Confusion Matrix")
plt.show()

print(classification_report(test_generator_balanced.classes, y_pred, target_names=labels))
```

    29/29 [==============================] - 4s 121ms/step
    


    
![png](output_59_1.png)
    


                  precision    recall  f1-score   support
    
          Castle       0.99      0.90      0.94       300
      Lighthouse       0.97      0.99      0.98       300
      Tree house       0.94      1.00      0.97       300
    
        accuracy                           0.96       900
       macro avg       0.96      0.96      0.96       900
    weighted avg       0.96      0.96      0.96       900
    
    


```python
# Predict and visualize
for label, path in custom_img_paths.items():
    print(f"\n🔍 True label: {label}")
    img_array, _ = get_img_array(path, size=(224, 224))

    preds = model_custom.predict(img_array)
    pred_class_idx = np.argmax(preds)
    pred_class_name = idx_to_class[pred_class_idx]

    print(f"Predicted class: {pred_class_name} ({preds[0][pred_class_idx]*100:.2f}%)")

    # Generate Grad-CAM
    heatmap = make_gradcam_heatmap(img_array, model_custom, last_conv_layer_name="conv2d_5")

    # Show image with heatmap
    display_gradcam(path, heatmap)
```

    
    🔍 True label: Castle
    1/1 [==============================] - 0s 338ms/step
    Predicted class: Castle (99.17%)
    


    
![png](output_60_1.png)
    


    
    🔍 True label: Lighthouse
    1/1 [==============================] - 0s 18ms/step
    Predicted class: Lighthouse (99.01%)
    


    
![png](output_60_3.png)
    


    
    🔍 True label: Tree house
    1/1 [==============================] - 0s 18ms/step
    Predicted class: Tree house (100.00%)
    


    
![png](output_60_5.png)
    


## Metadata

- What accuracy can be achieved?
  - For from scratch basically none, it just picks randomly
  - Pretrained (unbalanced) **(surprisingly good results)**
    - 100% test (not enough data!)
    - 97% val (not enough data!)
    - f1 score ~98% (68% for tree-house!)
  - Pretrained (balanced) **(also good model)**
    - 100% train
    - 93% val
    - f1 score 90-99% among classes
  - Experimental (balanced) **(best model)**
    - 99% train
    - 96% val
    - f1 score 94-98% among classes
- Infrastructure(s) used:
  - Tensorflow/Keras with CUDA (google-colab & docker tensorflow/tensorflow:2.14.0-gpu)
- Inference Time
  - GTX 1070ti ~18ms (a bit more if model needs to be loaded into VRAM first)
- Parameter Count
  - just see above... the .summary() shows all model details.


```python

```


```python

```
