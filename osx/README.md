# Installation in OSX

We have had success running PCprophet on OSX machines with the following conda creation steps:

```
conda create -n pcprophet
conda activate pcprophet
conda install python=3.7.16
conda install scikit-learn=1.0.2
conda install pandas=1.2.3
conda install networkx=2.4
conda install dask=2.30.0
conda install matplotlib=3.1.1


```


Alternatively, you can create the environment using the yml file included here.

```
conda env create -f pcprophet.osx.env.yaml

conda activate pcprophet
```

If your environment is successfully created, you should be able to cd to the main PCprophet directory,
(the directory where main.py is located)
and run PCprophet test as below:


```
conda activate pcrophet
cd [githubclonelocation]/PCprophet

python main.py -sid test/test_ids.txt -is_ppi False -db coreComplexes.txt

```
Output should be in the `Output/` directory and also some intermediate output files in `tmp/`