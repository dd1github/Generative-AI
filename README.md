# Generative-AI
Public repository for the paper "Generative AI Design and Exploration of Nucleoside Analogs".

## Abstract:

Nucleosides are fundamental building blocks of DNA and RNA in all life forms and
viruses. In addition, natural nucleosides and their analogs are critical in prebiotic chemistry, innate
immunity, signaling, antiviral drug discovery and artificial synthesis of DNA / RNA sequences.
Combined with the fact that quantitative structure activity relationships (QSAR) have been widely
performed to understand their antiviral activity, nucleoside analogs could be used to benchmark
generative molecular design. Here, we undertake the first generative design of nucleoside analogs
using an approach that we refer to as the Conditional Randomized Transformer (CRT). We also
benchmark our model against five previously published molecular generative models. We
demonstrate that AI-generated molecules include nucleoside analogs that are of significance in a
wide range of areas including prebiotic chemistry, antiviral drug discovery and synthesis of
oligonucleotides. Our results show that CRT explores distinct molecular spaces and chemical
transformations, some of which are similar to those undertaken by nature and medicinal chemists.
Finally, we demonstrate the potential application of the CRT model in the generative design of
molecules conditioned on Remdesivir and Molnupiravir as well as other nucleoside analogs with
in vitro activity against SARS-CoV-2. 

## Key Modules used to build CRT:

The key modules that were used with CRT are:

- Python 3.7
- Pytorch 1.9.0
- Rdkit 2020.09.10
- Tqdm 4.62.0
- pandas 1.2.5
- numpy 1.20.3

## Code description:
The code was largely developed and run on a single GeForce Nvidia RTX 3050 GPU with cuda toolkit version 11.1.1.

The code consists of three main files for model training, fine-tuning and molecule generation:

- Training.py
- Fine_tuning.py
- Generation.py

Generating molecules consists of three steps: 
1.	Training a model to learn the rules of chemical grammar by running train_main.py.  A pre-trained model is provided.  Training a model from scratch takes approximately 10-12 hours on a single GPU. 
2.	Fine tuning a model on a specific dataset of interest by running fine_tune.py.  A pre-trained model is provided.  The data must be downloaded, unzipped, placed in the appropriate folder and file addresses changed to run fine_tune.py.
3.	Generating molecules with generation.py.  

To run train_main.py, fine_tune.py, and generation.py, the data must be downloaded, unzipped, placed in the appropriate folders and folder addresses updated in the respective code files.

## Data and Pre-trained models:

The link to the data and pre-trained models is: (https://drive.google.com/drive/folders/11nWxBo8n29Jz9aHyOD1otHuC87M8iDQj?usp=sharing)

The data should be downloaded, unzipped and placed in the …/data folder.  The underlying training and validation SMILES data was taken from:  https://github.com/ETHmodlab/virtual_libraries.  The training and validation Morgan fingerprint property data was developed using Rdkit.

The pre-trained models should be downloaded, unzipped and placed in the …/models folder.

## Baseline models:

The baseline models can be found at the following links:

- *CRM*: https://github.com/ETHmodlab/virtual_libraries
- *LigGPT*:  https://github.com/devalab/molgpt
- *VAE, AAE, CRNN*: https://github.com/molecularsets/moses

## Cite:

If you find our research to be useful, please cite our publication: 

Dablain, Damien, Geoffrey Siwo, and Nitesh Chawla. "Generative AI Design and Exploration of Nucleoside Analogs." (2021).

































