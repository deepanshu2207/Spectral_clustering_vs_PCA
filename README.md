# Spectral_clustering_vs_PCA

Downloaded the Digits dataset from UCI Machine Learning Repository:
https://archive.ics.uci.edu/ml/datasets/Multiple+Features

This is an image data set which consists of features of handwritten numerals (0-9) extracted from a collection of Dutch utility maps with 200 patterns per class (for a total of 2,000 patterns), digitized as binary images. The dataset consists of the following six views:

i) mfeat-fou: 76 Fourier coefficients of the character shapes.
ii) mfeat-fac: 216 profile correlations.
iii) mfeat-kar: 64 Karhunen-Love coefficients.
iv) mfeat-pix: 240 pixel averages in 2 x 3 windows.
v) mfeat-zer: 47 Zernike moments.
vi) mfeat-mor: 6 morphological features.

Problem:
The dataset has k = 10 classes, one for each of the 10 digits (0-9). For each view, extract the k dimensional variance maximization subspace and also the k dimensional graph cut minimization subspace. Perform k-means clustering in both subspaces and assess the clustering performance using adjusted Rand index (ARI) or any other external cluster evaluation measure. You do not need to code for ARI or the k-means algorithm, you can use any standard implementation or package. You can use your choice of pairwise similarity measure for constructing the similarity graph. For each view, compare the clustering performance both subspaces, and report which one is better. Also, which subspace performs better in majority of the views.

Solution:
I have applied both the methods on the given data and got the results in PYTHON3. I have found that for some data files, PCA + k-means was good and for some data files, SC + kmeans was better. This shows the need of some unifying approach in multi-view subspace clustering. PCA performed better for Fourier coefficients, Profile Correlations, karhunen– love coefficients and morphological features. While Spectral Clustering performed better for pixels averages and Zernike moments. For exact values of accuracy, run the code.



























