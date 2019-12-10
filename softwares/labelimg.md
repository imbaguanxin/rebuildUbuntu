# labelimg install

first install anaconda3

then start anaconda

Then download the source code from github: https://github.com/tzutalin/labelImg

run following command:

```bash
cd ~/Downloads/labelImg-master
conda install pyqt=5
pyrcc5 -o libs/resources.py resources.qrc
python labelImg.py
```

Then it start to run. Please specify the input img folders and output xml folders.

short cut: `w` start to label, `a` previous pic, `d` next pic
