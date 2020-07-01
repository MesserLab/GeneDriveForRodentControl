# Modeling the potential of CRISPR gene drives for rodent management

<hr style=\"border:3px solid gray\"> </hr>

Files and data to accompany "Modeling the potential of CRISPR gene drives for rodent management".

The "Figures" folder contains high resolution verisons of the figures used in the paper.

The "Animnations" folder contains severeal animated 3-at-a-time analyses to augment the analyses done in the paper.

The "Data" folder contains data used to train and test the gaussian process models.

The "Models" folder contains pre-trained GPyTorch models. These models are not human readable.

Scripts and code in this repository:
- "rat_gene_drive_model.slim": the population model used in the paper.
- "rat_gp.py": the code for the GP models.
- "rat_plot.py": plotting functions for use with the GP models.
- "GeneDriveForRodentControl.ipynb": a jupyter notebok that can load the pretrained models, which can then generate additional sensitivity analyses, two-at-a-time plots, or three-at-a-time animations. No programming experience is necessary to use this notebook, and the ploting functionality is easy to use.

___
## Requirements
Running the population model requires the SLiM evolutionary simulation framework. https://messerlab.org/slim/

Loading the models in a jupyter notebook has a number of requirements:
- Python 3.6 or 3.7 (3.8 is not verified to work): https://www.python.org/downloads/.
- The following python packages:
  - Jupyter notebook: install via running ``pip install jupyterlab`` in a terminal or command prompt window or by other means.
  - Numpy: install via ``pip install numpy`` or by other means.
  - Pandas: install via ``pip install pandas`` or by other means.
  - Matplotlib: install via ``pip install matplotlib`` or by other means.
  - PyTorch: install varies from machine to machine, see https://pytorch.org/get-started/locally/ to configure the required command for your machine. If you want to accelerate the code with your GPU for potentially much faster runtimes, install NVidia's CUDA toolkit first: https://developer.nvidia.com/cuda-downloads.
  - GPyTorch: install via ``pip install gpytorch``. Install only after installing torch.
  - SALib: install via ``pip install SALib`` or by other means.

Saving animated 3-at-a-time heatmap plots also requires ffmpeg. Generating the plots and viewing them within the notebook does not require this. https://ffmpeg.org/download.html

___
## Running the notebook
After requirements are installed, the jupyter notebook can be run by opening a terminal or command prompt in the folder with these files, and running:

```
jupyter notebook GeneDriveForRodentControl.ipynb
```

Instructions on using the GP models is present within the notebook.
