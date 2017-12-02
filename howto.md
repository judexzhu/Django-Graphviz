# How To

I install anaconda for my python environment.

## Switch to your virtualenv

on mac 

```
$ source activate myDjangoEnv
```


## Install Tools

### Install django_extensions

```
$ pip install django_extensions
```

Add `django_extensions` into the `INSTALLED_APPS` in the project's `settings.py`.


```python
INSTALLED_APPS = (
    ...
    'django_extensions',
    ...
)
```

### Install graphviz

If you installed `brew` but not `conda` , run :

```bash
$ brew update
$ brew install graphviz
```

else you install the `conda` (like me), the `brew` will break:

```bash
conda install -c anaconda graphviz
```

### Install pygraphviz

try:

```bash
$ pip install pygraphviz
```

if failed:

```bash
pip install --install-option="--include-path=/usr/local/include/" --install-option="--library-path=/usr/local/lib/" pygraphviz
```

else :

```bash
$ pip install pyparsing==1.5.7
$ pip install pydot
```

>Note: I've not tried this way yet.

## Draw the models relation

Got to your Django Project folder:

```bash
python manage.py graph_models -a -o models.png
```


Example:

<img src=models.png>