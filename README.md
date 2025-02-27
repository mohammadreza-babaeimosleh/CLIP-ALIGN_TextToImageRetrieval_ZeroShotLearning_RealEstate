# CLIP-ALIGN_ZeroShotLearning_RealEstate
this repository Implements Zeroshot learning on a custom dataset of real-estate images (which could be replaced with any data) for TextToImage retrieval tasks. This repository contains a .ipynb (instead of.py) to help the process be more descriptive, but you can use it in .py format too (if you only want to see the final result)
##### Note: the data used is private and cannot be shared but there is no limit to it

# How to use
Just make a copy of the .ipynb file and try to run the cells :) if you want to use a .py file you should install the libraries installed at the first cell. Also, edit the path to your target images. Finally, replace the query with your desired text input (the object or concept that you are looking for in images)
##### Note: if you want to use CPU instead of GPU you should install a GPU version of the 'faiss' library (use the command below)

```bash
pip install faiss-cpu 
```

# Code description
The code downloads models and modifies your input to be proper for embedding. after doing the embedding properly embedding everything is ready to use. the code gets your input ('query' variable), does the similarity search for all the images in your data folder, and retrieves the images sorted by the amount of relevance between your query and the image. the relevance is measured by the 'Cosine Similairy' Score between the embedded version of your text input and images.
