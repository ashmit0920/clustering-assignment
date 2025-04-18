# clustering-assignment

Comparitive performance study of different clustering algorithms using different pre-processing techniques with different numbers of clusters on different evaluation parameters


## Dataset Used
- Heart Failure Clinical Records: https://archive.ics.uci.edu/dataset/519/heart+failure+clinical+records
- Number of instances: 299
- Number of Features: 12


## Algorithms
1. K-means Clustering
2. Hierarchical Clustering
3. K-means shift Clustering


## Preprocessing Techniques Used:
1. No Data Processing: Just runs clustering without any preprocessing
2. Normalization: Uses Z-score normalization.
3. Transformation: Applies Yeo-Johnson transformation
4. PCA: Reduces dimensionality with Principal Component Analysis
5. Normalization + Transformation: Applies both normalization and transformation
6. Normalization + PCA: Combines normalization with PCA for dimensionality reduction
7. Transformation + PCA: Applies both transformation and PCA
8. Normalization + Transformation + PCA: Uses all three preprocessing steps together

## Results
Models are created using different preprocessing techniques and different number of clusters (3,4,5). The results are as follows:

### K-Means Clustering

| Parameters          | No data preprocessing c=3 | No data preprocessing c=4 | No data preprocessing c=5 | Normalisation c=3 | Normalisation c=4 | Normalisation c=5 | Transformation c=3 | Transformation c=4 | Transformation c=5 | PCA c=3 | PCA c=4 | PCA c=5 | N+T c=3 | N+T c=4 | N+T c=5 | N+PCA c=3 | N+PCA c=4 | N+PCA c=5 | T+PCA c=3 | T+PCA c=4 | T+PCA c=5 | N+T+PCA c=3 | N+T+PCA c=4 | N+T+PCA c=5 |
|---------------------|---------------------------|---------------------------|---------------------------|-------------------|-------------------|-------------------|---------------------|---------------------|---------------------|---------|---------|---------|---------|---------|---------|------------|------------|------------|------------|------------|------------|--------------|--------------|--------------|
| Silhouette          | 0.5108                    | 0.5532                    | 0.5473                    | 0.1025            | 0.0885            | 0.0978            | 0.5182              | 0.5686              | 0.5810              | 0.5481  | 0.4789  | 0.5375  | 0.1012  | 0.0950  | 0.0898  | 0.0937     | 0.1011     | 0.0950     | 0.5553     | 0.5700     | 0.5957     | 0.1048       | 0.0957       | 0.0905       |
| Calinski-Harabasz   | 378.9268                  | 499.8170                  | 596.5868                  | 34.7313           | 28.0109           | 26.8731           | 424.4988            | 630.9197            | 727.3318            | 390.9995| 382.0646| 556.0944| 36.1264 | 29.0917 | 26.5525 | 34.1328    | 28.4765    | 26.5464    | 476.7125   | 605.3132   | 797.0873   | 36.1672      | 30.6920      | 26.8621      |
| Davies-Bouldin      | 0.6244                    | 0.5760                    | 0.5092                    | 2.3278            | 2.4916            | 2.2061            | 0.5943              | 0.5524              | 0.5487              | 0.5652  | 0.5907  | 0.5772  | 2.4842  | 2.7005  | 2.5896  | 2.4318     | 2.5271     | 2.4426     | 0.5659     | 0.4841     | 0.5019     | 2.4789       | 2.4241       | 2.6663       |


### Hierarchical Clustering

| Parameters          | No data preprocessing c=3 | No data preprocessing c=4 | No data preprocessing c=5 | Normalisation c=3 | Normalisation c=4 | Normalisation c=5 | Transformation c=3 | Transformation c=4 | Transformation c=5 | PCA c=3 | PCA c=4 | PCA c=5 | N+T c=3 | N+T c=4 | N+T c=5 | N+PCA c=3 | N+PCA c=4 | N+PCA c=5 | T+PCA c=3 | T+PCA c=4 | T+PCA c=5 | N+T+PCA c=3 | N+T+PCA c=4 | N+T+PCA c=5 |
|---------------------|---------------------------|---------------------------|---------------------------|-------------------|-------------------|-------------------|---------------------|---------------------|---------------------|---------|---------|---------|---------|---------|---------|------------|------------|------------|------------|------------|------------|--------------|--------------|--------------|
| Silhouette          | 0.5035                    | 0.5395                    | 0.5410                    | 0.0924            | 0.0850            | 0.0934            | 0.5189              | 0.5408              | 0.5639              | 0.5035  | 0.5395  | 0.5410  | 0.0693  | 0.0587  | 0.0604  | 0.0924     | 0.0850     | 0.0934     | 0.5189     | 0.5408     | 0.5639     | 0.0693       | 0.0587       | 0.0604       |
| Calinski-Harabasz   | 322.0706                  | 478.6348                  | 558.5869                  | 27.4504           | 25.3112           | 23.8345           | 467.7175            | 497.6851            | 723.6225            | 322.0706| 478.6348| 558.5869| 27.6672 | 23.6416 | 21.1210 | 27.4504    | 25.3112    | 23.8345    | 467.7175   | 497.6851   | 723.6225   | 27.6672      | 23.6416      | 21.1210      |
| Davies-Bouldin      | 0.5560                    | 0.5775                    | 0.4900                    | 2.5744            | 2.1641            | 2.0229            | 0.6099              | 0.5251              | 0.4999              | 0.5560  | 0.5775  | 0.4900  | 2.8704  | 2.6958  | 2.8859  | 2.5744     | 2.1641     | 2.0229     | 0.6099     | 0.5251     | 0.4999     | 2.8704       | 2.6958       | 2.8859       |

### K-Means Shift Clustering

| Parameters          | No data preprocessing c=3 | No data preprocessing c=4 | No data preprocessing c=5 | Normalisation c=3 | Normalisation c=4 | Normalisation c=5 | Transformation c=3 | Transformation c=4 | Transformation c=5 | PCA c=3 | PCA c=4 | PCA c=5 | N+T c=3 | N+T c=4 | N+T c=5 | N+PCA c=3 | N+PCA c=4 | N+PCA c=5 | T+PCA c=3 | T+PCA c=4 | T+PCA c=5 | N+T+PCA c=3 | N+T+PCA c=4 | N+T+PCA c=5 |
|---------------------|---------------------------|---------------------------|---------------------------|-------------------|-------------------|-------------------|---------------------|---------------------|---------------------|---------|---------|---------|---------|---------|---------|------------|------------|------------|------------|------------|------------|--------------|--------------|--------------|
| Silhouette          | 0.6159                    | 0.6159                    | 0.6159                    | 0.2683            | 0.2683            | 0.2683            | 0.4507              | 0.4507              | 0.4507              | 0.6159  | 0.6159  | 0.6159  | 0        | 0        | 0        | 0.2683     | 0.2683     | 0.2683     | 0.4507     | 0.4507     | 0.4507     | 0            | 0            | 0            |
| Calinski-Harabasz   | 79.4950                   | 79.4950                   | 79.4950                   | 7.4673            | 7.4673            | 7.4673            | 143.1638            | 143.1638            | 143.1638            | 79.4950 | 79.4950 | 79.4950 | 0        | 0        | 0        | 7.4673     | 7.4673     | 7.4673     | 143.1638   | 143.1638   | 143.1638   | 0            | 0            | 0            |
| Davies-Bouldin      | 0.2587                    | 0.2587                    | 0.2587                    | 0.7525            | 0.7525            | 0.7525            | 0.4277              | 0.4277              | 0.4277              | 0.2587  | 0.2587  | 0.2587  | 0        | 0        | 0        | 0.7525     | 0.7525     | 0.7525     | 0.4277     | 0.4277     | 0.4277     | 0            | 0            | 0            |



1. K-Means Clustering: Works best with transformation and number of clusters=5

![newplot](https://github.com/user-attachments/assets/b5fff168-b2da-4359-b154-765975e3f823)


2. Hierarchical Clustering: Provides best performance with Transformation or Transformation+PCA, with 5 clusters.

  ![newplot (1)](https://github.com/user-attachments/assets/33de93ef-3dc0-4187-9e58-1b8dc36a5fac)


3. K-Means Shift Clustering: Performs best without any preprocessing for 3/4/5 number of clusters. PCA also provides similar results
   
![newplot (2)](https://github.com/user-attachments/assets/59eb4a74-d66a-4110-8b72-f7993655c232)
