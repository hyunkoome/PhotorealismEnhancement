## Setup

The code has been developed using a conda environment:
```shell
conda create -n photoreal python==3.8
conda activate photoreal
```    
    

You'll need pytorch, scikit-image, imageio, tqdm:
```shell
pip install torch==2.1.1 torchvision==0.16.1 torchaudio==2.1.1 --index-url https://download.pytorch.org/whl/cu121
pip install -r ./code/requirements.txt
```
    
- Training requires 
  - [MSeg](https://github.com/mseg-dataset/mseg-semantic) for generating robust labels of a dataset, 
  - [faiss](https://github.com/facebookresearch/faiss) for matching crops across datasets, 
  - and [LPIPS](https://github.com/richzhang/PerceptualSimilarity) for the perceptual loss. 
  - The code contains optional downsampling using [Kornia](https://github.com/kornia/kornia) for the perceptual loss and the discriminator.- 
- Once you execute `pip install -r ./code/requirements.txt`, install faiss, lpips, kornia packages as well. 
- If you do not wish to use it (it is disabled by default), you may remove this dependency.- 
- Please refer to the respective websites for up-to-date installation instructions.

After installing all the prerequisites, install the epe package (editable) locally:
```shell
pip install -e ./code/
```
    
