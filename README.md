# Tomato Leaf Lesion Segmentation Dataset

Data resources for **MVMamba-Seg: A precise multimodal segmentation method for tomato disease monitoring via efficient Vision Mamba**.

## Release status

The dataset is being prepared for public release. This repository will provide the self-built tomato leaf images and lesion masks, newly created lesion masks for the selected PlantVillage images, and image lists defining the evaluation partitions.

## Dataset overview

The task is binary segmentation of diseased regions on tomato leaves. Both datasets cover five disease categories:

| Disease | Self-built images | PlantVillage images |
| --- | ---: | ---: |
| Bacterial spot | 208 | 598 |
| Early blight | 213 | 585 |
| Late blight | 205 | 612 |
| Leaf mold | 196 | 641 |
| Septoria leaf spot | 193 | 613 |
| **Total** | **1,015** | **3,049** |

The self-built images were collected in collaboration with the Plant Protection Research Institute of the Hunan Academy of Agricultural Sciences. PlantVillage provides images captured under controlled conditions. Lesion annotations were prepared by plant and plant-disease experts using LabelMe.

## Evaluation partitions

The self-built dataset is divided into training, validation, and test subsets at an approximately 8:1:1 ratio. The release will include the fixed image lists used in the study.

All 3,049 selected PlantVillage images are used for cross-domain testing. They are excluded from model training and validation.

## Planned repository structure

```text
Tomato-Leaf-Lesion-Segmentation/
├── README.md
├── selfbuilt/
│   ├── images/
│   └── masks/
├── plantvillage/
│   ├── masks/
│   └── image_mapping.csv
├── splits/
│   ├── selfbuilt_train.txt
│   ├── selfbuilt_val.txt
│   ├── selfbuilt_test.txt
│   └── plantvillage_test.txt
└── metadata.csv
```

Image-to-mask correspondence, mask encoding, and metadata fields will be documented with the release. `image_mapping.csv` will identify the corresponding original PlantVillage files.

## PlantVillage image source

Original PlantVillage images are available from the [PlantVillage dataset repository](https://github.com/spMohanty/PlantVillage-Dataset). This repository provides the new lesion masks and their image correspondence.



