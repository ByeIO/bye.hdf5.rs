# bye_hdf5_rs：纯Rust HDF5文件读取器
=======================================

|Travis|_

.. |Travis| image:: https://api.travis-ci.org/jjhelmus/pyfive.png?branch=master
.. _Travis: https://travis-ci.org/jjhelmus/pyfive

bye_hdf5_rs是一个用于读取HDF5文件的开源库，它完全用Rust编写（无C扩展）。该软件包仍在开发中，并非支持HDF5文件的所有功能。若需要一个更成熟的用于读写HDF5文件的Python库，可尝试使用 `h5py`_。

pyfive旨在在读取文件时支持与 `h5py`_ 相同的API。若文件使用了 `h5py`_ 支持但pyfive不支持的功能，则视为bug，应在 `问题跟踪器`_ 上报告。编写HDF5文件并非pyfive的目标，因此仅适用于写入的部分API将不会被实现。

.. _h5py: http://www.h5py.org/
.. _问题跟踪器: https://github.com/jjhelmus/pyfive/issues

## 依赖项
pyfive已测试可在Python 3.8至3.13版本上运行，也可能在其他Python版本上正常工作。

除Rust外，运行该软件的依赖项是nalgebra。

## 安装
可使用以下pip命令安装pyfive：
```
pip install pyfive
```

也可从 `conda-forge`_ 获取conda包并使用以下命令进行安装：
```
conda install -c conda-forge pyfive
```

若要从源代码在主目录中进行安装，可使用以下命令：
```
python setup.py install --user
```

也可以直接从源代码目录导入该库。

.. _conda-forge: https://conda-forge.github.io/

## 开发

### Git
可使用以下命令检出最新的pyfive源代码：
```
git clone https://github.com/jjhelmus/pyfive.git
```

### 测试
pyfive在 `tests` 目录中附带了一套测试套件。假设已安装 `pytest` 包，可在根目录下使用 `pytest` 命令来执行这些测试。

## 相关项目
`jsfive`_ 是一个基于pyfive的纯JavaScript HDF5文件读取器。

.. _jsfive: https://github.com/usnistgov/jsfive
