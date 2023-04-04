# MINING-GOLD-FROM-GENERATORS

Mining gold from implicit models to improve likelihood-free inference, example for ROLR and RASCAL.

## Paper

[Mining gold from implicit models to improve likelihood-free inference](https://arxiv.org/pdf/1805.12244.pdf)<br>
by: Johann Brehmer, Gilles Louppe, Juan Pavez, and Kyle Cranmer

### Abstract

Simulators often provide the best description of real-world phenomena. However, the density they implicitly define is often intractable, leading to challenging inverse problems for inference. Recently, a number of techniques have been introduced in which a surrogate for the intractable density is learned, including normalizing flows and density ratio estimators. We show that additional information that characterizes the latent process can often be extracted from simulators and used to augment the training data for these surrogate models. We introduce several new loss functions that leverage this augmented data, and demonstrate that these new techniques can improve sample efficiency and quality of inference.

## Key Idea

By extracting more information from the generator, the regression on the likilhood becomes more data efficient since the 
possible functions that describe the likelihood ratio are narrowed down to a smaller corridor which the NN has to optimize for.<br>
Additional information that is extracted is the ratio of the pdf during the data generating process $r(x)$ and the score function $t(x)$ which is the deriative of the pdfs.  

### Cite Key

```
@article{Brehmer_2020,
	doi = {10.1073/pnas.1915980117},
  
	url = {https://doi.org/10.1073%2Fpnas.1915980117},
  
	year = 2020,
	month = {feb},
  
	publisher = {Proceedings of the National Academy of Sciences},
  
	volume = {117},
  
	number = {10},
  
	pages = {5242--5249},
  
	author = {Johann Brehmer and Gilles Louppe and Juan Pavez and Kyle Cranmer},
  
	title = {Mining gold from implicit models to improve likelihood-free inference},
  
	journal = {Proceedings of the National Academy of Sciences}
}
```