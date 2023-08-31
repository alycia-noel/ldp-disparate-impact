# Randomized Response Has No Disparate Impact on Model Accuracy
Code repository for paper submitted to IEEE Big Data 2023 held in Sorrento, Italy. 

### Dependencies
- python: 3.9.15
- numpy: 1.23.5
- pandas: 1.5.2
- torch: 1.13.0
- torchvision: 0.14.0
- matplotlib: 3.6.2
- pillow: 9.3.0
- seaborn: 0.12.1
- scienceplots: 2.0.1
- scikit-learn: 1.1.3
- lightgbm: 4.0.0
- folktables: 0.0.12
- xxhash: 3.2.0
- fire: 0.5.0

### How to run
The name of each .ipynp file details what experiments are run in that specific jupyter notebook. For example, Income.ipynp contains the code to run all experiments on the ACSIncome dataset and utkface-vgg.ipynp contains the code to run experiments on the UTKFace dataset using VGG as the underlying model. The two image dataset files (e.g., utkface-X.ipynp and cimnist-X.ipynp) can be run without any modifications. The remaining three files (Employ.ipynp, Income.ipynp, and PubCov.ipynp) can be run with minor modifications to the last cell. Specifically, to choose what experiment to run, change _which_set = 'lab'_ in line 2 to be ['lab', 'feat', 'feat-lab'] depending on if randomization should be performed on the labels, the features, or the features and labels. The graphs shown in the paper can be generated using graphing-final.ipynp. Finally, if the CI-MNIST dataset needs to be reconstructed, the generate-ci-mnist.ipynb can be used with minor modifications made to the directory paths. 
