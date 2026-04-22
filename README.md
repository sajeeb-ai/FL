# FL - Fedarated Learning Project


We implement a privacy-preserving federated-style pipeline for pneumonia detection using PneumoniaMNIST. Raw client images are kept local, while each client extracts frozen DenseNet features, applies local debiasing and clipping, and shares only private per-class Gaussian mixture summaries instead of raw data.

At the server side, these client summaries are aligned and aggregated to form global class distributions, which are then used together with replayed feature representations to train a conditional diffusion-based feature generator. Synthetic features sampled from this generator are used to train a downstream classifier, and the results are compared against a real-feature baseline using validation and test metrics such as AUC, accuracy, recall, specificity, F1-score, and balanced accuracy.

Overall, the notebook focuses on evaluating whether privacy-aware feature synthesis can approximate the performance of a classifier trained on real feature representations while avoiding direct sharing of raw medical images.

continue...
