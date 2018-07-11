# Id a whale

## Project Instructions

1. Clone the repository and navigate to the downloaded folder.

```bash
git clone git@github.com:crawlik/whale-id.git
cd whale-id
```

2. Create and activate a new environment.

```bash
conda create -y -n whale-id python=3.6
source activate whale-id
pip install -r requirements.txt
# Optional: install optimized TF from https://github.com/lakshayg/tensorflow-build
# 2.9 GHz Intel Core i7, OSX Sierra
pip install --ignore-installed --upgrade "https://github.com/lakshayg/tensorflow-build/raw/master/tensorflow-1.8.0-cp36-cp36m-macosx_10_7_x86_64.whl"
```

3. Download the data

You may need to install Kaggle API key.

```bash
kaggle competitions download -c whale-categorization-playground --wp
unzip train.zip
unzip test.zip
```

4. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `quadcop` environment.
```bash
python -m ipykernel install --user --name whale-id --display-name "whale-id"
```

5. Open the notebook.
```
jupyter notebook whale-id.ipynb
```
Running notebook remotely on a headless server.
```
jupyter notebook --ip=0.0.0.0 --no-browser whale-id.ipynb
```


5. Before running code, change the kernel to match the `quadcop` environment by using the drop-down menu (**Kernel > Change kernel > whale-id**). Then, follow the instructions in the notebook.

6. You will likely need to install more pip packages to complete this project.  Please curate the list of packages needed to run your project in the `requirements.txt` file in the repository.
