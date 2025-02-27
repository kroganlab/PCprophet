# PCprophet

Software toolkit for protein complex prediction and differential analysis of cofractionation mass spectrometry datasets.

## 


## Docker Instructions


To run from the  Docker image on Docker hub:

```
docker  run -it -v`pwd`:/wd -w /wd martingordon808/condapcprophet python main.py -sid test/test_ids.txt -is_ppi False -db coreComplexes.txt
```

If that doesn't work, you may have to build the docker image locally. After downloading the source code (see section *Command line version*), run

```
docker  build PCprophet/dockerEnv/ -t bpolacco/condapcprophet
```

You can change `bpolacco/condapcprophet` to any tag (name) you want. Then retry the docker run command above.


## Getting Started


These instructions will guide you to obtain a copy of the project, to run on your local machine, and to test the compatibility with your current Python packages.

### Dependencies

These are be outdated and incomplete.  See `osx/` directory for an example of setting up a conda environment.

* [Python >=3.4.x](https://www.python.org)
* [Sklearn 0.23.2](https://pypi.org/project/sklearn/)
* [NetworkX v2.4](https://networkx.github.io)
* [Pandas >=1.23](https://pandas.pydata.org)
* [Scipy >=1.5.2](https://www.scipy.org)
* [Dask >=2.30.0](https://dask.org)

### Installing

We recommend using [anaconda](https://www.anaconda.com) as it contains the majority of the required packages for PCprophet. If you are using Windows and having problems adding paths of anaconda and Python, please click [here](https://www.datacamp.com/community/tutorials/installing-anaconda-windows) for guidance. Please also refer to this [page](https://stackoverflow.com/questions/54063285/numpy-is-already-installed-with-anaconda-but-i-get-an-importerror-dll-load-fail) for potential errors when importing python packages in Windows.

#### OSX

A conda environment tested on OSX can be found in the `osx/` directory.

#### Command line version

Ensure that you have installed the GitHub tool and 'git-lfs' command specifically for large file transfer. Please see [here](https://gist.github.com/derhuerst/1b15ff4652a867391f03) for installing GitHub and [here](https://help.github.com/en/github/managing-large-files/installing-git-large-file-storage) for the installing 'git-lfs' command.

```
git clone https://github.com/kroganlab/PCprophet PCprophet
```
This will get you a working copy of PCprophet into a folder called PCprophet. Please go to the 'PCprophet' folder to unzip 'tmp_GO_sp_only.txt.zip'. You then should be able to see the tmp_GO_sp_only.txt file in the same folder. Note that the 'tmp_GO_sp_only.txt' file must be under the 'PCprophet' folder.

## Usage

For usage of PCprophet, refer to the [PCprophet_instructions.md](https://github.com/anfoss/PCprophet/blob/master/PCprophet_instructions.md).

## Running PCProphet on Wynton

As Docker is not available on Wynton, you will need to use Singularity to build the PCprophet container. Singularity can pull Docker images from remote repositories including Dockerhub and convert to Singularity containers. First, ensure you have installed the necessary dependencies and cloned the `PCprophet` repository following the *Command line version* instructions above.  Move into the `PCprophet` folder and run the following:
```
singularity run -B $PWD docker://martingordon808/condapcprophet:latest python main.py -sid test/test_ids.txt -is_ppi False -db coreComplexes.txt
```

## Contributing

Please read [CONTRIBUTING.md](https://github.com/anfoss/PCprophet/blob/master/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.


## Authors

* **Andrea Fossati** - *Initial work* - [anfoss](https://github.com/anfoss) andrea.fossati@ucsf.edu
* **Chen Li** - *Initial work* - chen.li@monash.edu


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

PCprophet citation:

Fossati, A., Li, C., Uliana, F., Wendt, F., Frommelt, F., Sykacek, P., Heusel, M., Hallal, M., Bludau, I., Capraz, T., Xue, P., Song, J., Wollscheid, B., Purcell, A. W., Gstaiger, M., & Aebersold, R. (2021). PCprophet: a framework for protein complex prediction and differential analysis using proteomic data. Nature Methods, 13. https://doi.org/10.1038/s41592-021-01107-5

## Acknowledgments

* [mojaje](https://github.com/mojaie/pygosemsim) for the implementation of GO tree parsing.
