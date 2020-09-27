## Segmentation with Unet

Unet is a convolutional neural network developed by [Ronnenberg et al, 2015](https://arxiv.org/abs/1505.04597), with the shape of an autoencoder containing multiple skip connections. It was initially designed for segmenting biomedical images.

The code presented in this repository has been designed such that: 
1. the architecture of Unet can be easily modified with different kernel sizes (`--kernel_size`), kernel number (`--kernel_num`), number of layers (`--depth`) 
2. the optimisation part can also be easily modified with various optimisers (`--optim`)
3. the results are all saved in `.npz` that can be processed with the script: `read_experiments.py` (not everything is working though, I am working on it). 

However, the last activation layer and loss function have to be modified to handle binary images. 

### Before running any script
- One external file and one external folder are required outside this repository: the file `boulders.pkl`, and the folder `experiments`.

### Running and processing an experiment
- `python main.py`, followed by different options. Run Unet on the images. Results are saved as `exp_x`, with `x` the experiment number.
- `python read_experiments.py --nb x`, process the results. `x` being the number of the folder, in `exp_x`.

# May the force be with you
