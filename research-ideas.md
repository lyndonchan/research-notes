Research Ideas
* Competitive methods for WSSS from image-level labels: PRM and successor, PSA and successor
* HSN-v2
    ** CNN+Grad-CAM+CRF: end-to-end training with learnable BG/OT activations (ADP tuning), loss function to maximize single pixel confidence, global pixel confidence, minimize Grad-CAM overlapping, intra-segment visual heterogeneity (reduce CRF changes) (ADP training)
    ** CNN+Attention Mechanism+Grad-CAM+CRF: end-to-end training, with progressive weighting with attention mechanism
    ** CNN+Multi-Scale Grad-CAM+CRF: end-to-end training, with amalgamation of Grad-CAM at multiple scales
    ** CNN+Grad-CAM+Random Walk+CRF: end-to-end training, with random walk outward/inward from seeds
* Multi-Label Pixel-Preserving Data Augmentation: implement training that uses Grad-CAM progressively to eliminate GT labels that are cut off by image augmentation transformations

* Reading
** Boykov and Partial Cross-Entropy Loss

* Evaluation
** Other WSSS methods: lots of Grad-CAMs overlap in pathology, but not in natural scene images