# 🧠 MNIST Handwritten Digit Classification Project

## 📋 Project Description

This project is part of the **Applied Artificial Intelligence** course (June 2025) at **ETSI Industriales (UPM)**. The objective is to compare different classification techniques for recognizing handwritten digits from the **MNIST dataset**.

Each digit is represented as a vector of **784 components** (**28×28 pixel** images). **10,000 labeled samples** are available for training and testing.

## 👥 Team Members

| **Role**         | **Student**                 |
|------------------|-----------------------------|
| Coordinator      | Martín Loring Bueno         |
| Scientist        | David Laborda Izquierdo     |
| Technician       | Diego Ramírez Fuente        |

## 🧠 Implemented Techniques

### 🔧 Preprocessing
- **PCA** (Principal Component Analysis)
- **LDA** (Linear Discriminant Analysis) with clustering (k-means)
- **Autoencoder** (non-linear)
- Data normalization
- Data split (**90% train, 10% test**)

### 🎯 Classifiers
- **k-NN** (k-Nearest Neighbors)
- **Bayesian Classifier**
- **MLP** (Multilayer Perceptron)
- **SOM** (Self-Organizing Maps)
- **CNN** (Convolutional Neural Network)

## 📊 Obtained Results

| **Method**           | **Accuracy (%)** | **Training Time (s)** | **Test Time (s)** |
|----------------------|------------------|------------------------|-------------------|
| PCA + k-NN           | 94.98            | 0.004                  | 0.021             |
| LDA + k-NN           | 95.70            | 0.004                  | 0.033             |
| PCA + LDA + k-NN     | 95.58            | 0.004                  | 0.023             |
| PCA + AE + k-NN      | 94.38            | 0.016                  | 0.2               |
| PCA + Bayes          | 87.20            | 0.020                  | 0.034             |
| LDA + Bayes          | 86.70            | 0.016                  | 0.027             |
| PCA + LDA + Bayes    | 86.76            | 0.019                  | 0.023             |
| PCA + AE + Bayes     | 82.42            | 1.442                  | 19.782            |
| PCA + MLP            | 95.07            | 48.47                  | 0.020             |
| LDA + MLP            | 94.95            | 56.19                  | 0.020             |
| PCA + LDA + MLP      | 94.66            | 42.61                  | 0.020             |
| PCA + SOM            | 90.60            | 48.67                  | 0.030             |
| LDA + SOM            | 33.50            | 18.00                  | 0.023             |
| PCA + LDA + SOM      | 32.92            | 18.32                  | 0.020             |
| **DLN (CNN)**        | **98.67**        | **334.0**              | **0.57**          |

## 📁 File Structure

### 💻 MATLAB Code (.mlx)
- `Tabajo_TamañoTesting.mlx` - Test set size analysis
- `Tabajo_SOM.mlx` - Self-Organizing Maps implementation
- `Tabajo_NormVsNo.mlx` - Normalized vs non-normalized data comparison
- `Tabajo_MLP.mlx` - Multilayer Perceptron implementation
- `Tabajo_KNN_BAY_PCA_LDA.mlx` - k-NN and Bayes with PCA/LDA implementation
- `Tabajo_DL.mlx` - Deep neural network implementation
- `Tabajo_ComparacionNumeroSubclases.mlx` - Subclass number analysis
- `predictor_datos_profe.mlx` - Final classifier for unknown data

### 📊 Results Files (.mat)
- `Group02_mlp.mat` - MLP results
- `Group02_som.mat` - SOM results
- `Grupo02_bay.mat` - Bayesian classifier results
- `Grupo02_dln.mat` - Deep network results
- `Grupo02_knn.mat` - k-NN results

### 📄 Documentation
- `results group 02.docx` - Document with confusion matrices and final results

## 🎯 Conclusions

- **CNN** achieved the **best performance** (98.67% accuracy) despite longer training time
- **k-NN** showed a good balance between accuracy and speed
- The **autoencoder** did not significantly improve results compared to PCA
- Data **normalization** did not improve results overall
- The **90%/10%** (train/test) split performed better than the typical 80%/20%

## 🔧 Requirements

- **MATLAB** (recommended version: R2021a or higher)
- **Toolboxes**:
  - Statistics and Machine Learning Toolbox
  - Deep Learning Toolbox
  - Neural Network Toolbox

## 📝 Usage

1. Clone the repository
2. Open **MATLAB** and navigate to the project directory
3. Execute the desired **.mlx** scripts
4. The **.mat** files contain trained models and results

## 📄 License

This project was developed as academic work for the **Polytechnical University of Madrid (UPM)**.
