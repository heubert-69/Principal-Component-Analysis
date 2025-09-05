## Face Recognition with PCA + Support Vector Classifier
📌 Project Overview

This project explores dimensionality reduction with Principal Component Analysis (PCA) combined with a Support Vector Classifier (SVC) for a multi-class face recognition task.

The dataset consists of labeled face images of public figures. The main goal was to apply PCA to reduce dimensionality (extracting principal components as features) and then classify individuals using SVC.

Even though my cross-validation scores showed relatively low accuracy, I carried the experiment forward to analyze how PCA + SVC performs on high-dimensional facial recognition.

⚙️ Methods Used

Preprocessing

Images were flattened into vectors.

Standard scaling applied before PCA.

Dimensionality Reduction (PCA)

Extracted principal components to capture the most variance in the dataset.

Reduced input feature space drastically, which is important for high-dimensional image data.

Classification (Support Vector Classifier)

Implemented a linear kernel SVC.

Cross-validation was used to tune parameters, though accuracy remained suboptimal.

Evaluation

Despite weak cross-validation scores, I evaluated the model on the test set.

Precision-Recall curves for each individual were plotted.

📊 Results

The precision-recall analysis showed mixed performance across different individuals. Some identities were classified with high average precision (AP close to 1.0), while others performed poorly (AP close to 0.1–0.3).

Example results (Average Precision per person):

✅ High performance:

Angelina Jolie (AP = 1.00)

Paul Bremer (AP = 1.00)

Gloria Macapagal Arroyo (AP = 0.94)

⚠️ Poor performance:

Ricardo Lagos (AP = 0.12)

Michael Bloomberg (AP = 0.18)

Atal Bihari Vajpayee (AP = 0.33)

Overall, the accuracy was inconsistent across classes, showing the challenges of working with limited samples and high intra-class variation in faces.

📈 Visualization

Below is the Precision-Recall Curve generated for the multi-class classification results:

📝 Conclusion

PCA helped reduce dimensionality significantly, but information loss affected classifier performance.

SVC worked better for some individuals than others, highlighting imbalanced data distribution and feature loss from PCA.

Even though cross-validation scores were not great, this experiment was a valuable learning step in understanding PCA + SVC on face datasets.

🚀 Future Improvements

Try Kernel PCA or t-SNE/UMAP for non-linear dimensionality reduction.

Use deep learning (CNNs) to automatically learn better features.

Experiment with data augmentation to handle class imbalance.
