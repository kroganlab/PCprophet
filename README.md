# PCprophet

Software toolkit for protein complex prediction and differential analysis of cofractionation mass spectrometry datasets

## Getting Started

These instructions will get you a copy of the project up and running on your local machine and how to test the compatibility with your current Python packages
### Prerequisites

* [Python 3.x](https://www.python.org)
* [Sklearn 0.20.3](https://pypi.org/project/sklearn/)
* [NetworkX >2.1](https://networkx.github.io)
* [Pandas >0.23](https://pandas.pydata.org)
* [Scipy >1.1.0](https://www.scipy.org)
* [Java v1.8](https://www.java.com)
* [Igraph](https://igraph.org/python/)

### Installing

We recommend using [anaconda](https://www.anaconda.com) as it contains the majority of the required packages for PCprophet, while igraph needs to be installed separately [here](https://igraph.org/python/)

#### Command line version

```
git clone https://github.com/fossatiA/PCprophet PCprophet
```
This will get you a working copy of PCprophet into a folder called PCprophet

> **note** for the command line version only Python3 and related package dependencies are necessary

#### GUI version


- Install Java v1.8
- Clone the repo

```
git clone https://github.com/fossatiA/PCprophet PCprophet
```
> **note** for the GUI version installtion of java is necessary

## Usage

For usage of PCprophet refers to the [PCprophet_instructions.md](https://github.com/fossatiA/PCprophet/blob/master/PCprophet_instructions.md)


## Built With

* [Pynstaller](https://www.pyinstaller.org) - Package builder
* [NetBeans](https://netbeans.org/) - GUI builder


## Contributing

Please read [CONTRIBUTE.md](https://github.com/fossatiA/PCprophet/blob/master/CONTRIBUTE.md) for details on our code of conduct, and the process for submitting pull requests to us.


## Authors

* **Andrea Fossati** - *Initial work* - [fossatiA](https://github.com/fossatiA) fossati@imsb.biol.ethz.ch
* **Chen Li** - *Initial work* - chen.li@monash.edu

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* [mojaje](https://github.com/mojaie/pygosemsim) for the implementation of GO tree parsing
