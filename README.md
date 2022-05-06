# Installing TF on m1

1. Install miniforge

```
chmod +x ~/Downloads/Miniforge3-MacOSX-arm64.sh
sh ~/Downloads/Miniforge3-MacOSX-arm64.sh
source ~/miniforge3/bin/activate
reload
```

2. Create a dir

```
mkdir tf-test
cd tf-test
```

3. Create new Conda environment

```
conda create --prefix ./env python=3.8
conda activate ./env
```

4. Install TF Dependencies from Apple's Conda channel

```
conda install -c apple tensorflow-deps
```

5. Install Apple's fork of TensorFlow

```
python -m pip install tensorflow-macos
```

6. Install Apple's tensorflow-metal. To allow usage of M1 GPUs

```
python -m pup install tensorflow-metal
```

7. Install other data science packages

```
conda install jupyter pandas numpy matplotlib scikit-learn
```

8. Start Jupyter Notebook

```
jupyter notebook
```
