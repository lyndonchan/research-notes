# Image Segmentation

* Graph theoretic segmentation
  * Normalized Cuts
  * Using textons (texture features)
* Segmentation as Energy Minimization
  * Grab Cut
  * Graph Cuts
  * Markov Random Fields (MRF) & Conditional Random Fields (CRF)
* Semantic Segmentation
  * Why?
    * Satellite imaging
	* Medical imaging
	* Facial detection and recognition
	* Image-based search
	* Retail and fashion
    * Robot vision and understanding
	* Autonomous driving
* Post-processing
  * "They [CRFs] can enforce global and local consistency of the predicted segments." Source: https://www.reddit.com/r/MachineLearning/comments/9e13kg/d_why_fully_connected_crf_help_in_sharp_labelling/
  * "The key idea of CRF inference for semantic labelling is to formulate the label assignment problem as a probabilistic inference problem that incorporates assumptions such as the label agreement between similar pixels." Source: https://www.robots.ox.ac.uk/~szheng/papers/CRFasRNN.pdf
  * "The pairwise energies provide an image data-dependent smoothing term that encourages assigning similar labels to pixels with similar properties." Source: https://www.robots.ox.ac.uk/~szheng/papers/CRFasRNN.pdf
  
* CRF papers to review
  * https://arxiv.org/pdf/1504.01013.pdf
  * https://arxiv.org/pdf/1503.02351.pdf

* *Source*: http://vision.stanford.edu/teaching/cs231b_spring1213/slides/segmentation.pdf

* Recurrent Instance Segmentation