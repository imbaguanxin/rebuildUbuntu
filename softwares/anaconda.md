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

Create a new environment for conda
```bash
conda create --name [new-environment-name]
```
