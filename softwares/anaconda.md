# anaconda

In mainland china: go to [tuna](https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/) to get the source.

```bash
cd ~/Downloads
sh Anaconda3-5.4.1-Linux-x86_64.sh
```

To use Anaconda:
```bash
source ~/anaconda3/bin/activate
```
mac:
```bash
source ~/opt/anaconda3/bin/activate
```

Or just type:
```bash
conda activate [environment-name]
```

Stop anaconda from starting environment once open the Terminal:
```bash
conda config --set auto_activate_base false
```

leave anaconda environment:
```bash
conda deactivate
```

## Commonly used commands

* `conda create --name [new-env]`: create a new environment.
* `conda env list` list environments.
* `conda --version`: see version of conda
* `conda install [lib-name]=[version]` install conda package. use strings like `'bar-lib>1.3.4,<1.1'` or `'bar-lib=1.0|1.4*'` to specify the version.
* `conda update [lib-name]` update conda package.
* `conda remove [lib-name]` remove package
* `conda search [lib-name]` search info of given package. `conda search cytoolz=0.8.2 --info` to show information of specific package of specific version out on web.
* `conda list` shows all packages installed. 
  * `conda list 'numpy|pandas'` list packages you want to see.
  * `conda list --name [env-name] 'numpy|pandas'`list packages on certain environment


## advanced usages

* `anaconda search [lib-name]` anaconda-client package help search all available packages with much information.
* `conda install -c [organization] [lib]` install packages on channels other than the base channel.
* `conda env remove -n [env-name]` remove specific environment.
* `conda create --name [new-env-name] [libname]=[version] [libname]=[version] ...`
* `conda env export -n [env-name] -f [file-name]` export environment to a file (.yml)
* `conda env create -n [name] -f [filename]` create environment from file(.yml)