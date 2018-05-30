### pyenv

```
$ git clone https://github.com/yyuu/pyenv.git ~/.pyenv

$ echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile
$ echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile
$ echo 'eval "$(pyenv init -)"' >> ~/.bash_profile
$ source ~/.bash_profile
```

Check whether pyenv is installed successfully
```
$ pyenv --help
```

Check the list of versions (very long list)
```
$ pyenv install --list
```

Now you can install the versions you want, e.g.:
```
pyenv install -v 3.6.5
pyenv install -v 2.7.15
```

### virtualenv

virtualenv can be used independently, but with pyenv, we
install pyenv-virtualenv plugin for virtualenv usage. 

```
$ git clone https://github.com/yyuu/pyenv-virtualenv.git $(pyenv root)/plugins/pyenv-virtualenv

$ echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.bash_profile
$ source ~/.bash_profile
```

Check whether pyenv-virtualenv is installed successfully
```
$ pyenv help virtualenv
```

Usage:
```
$ pyenv virtualenv <python version> <project env name>
```

Examples:
```
$ pyenv virtualenv 2.7.15 env-py2
$ pyenv virtualenv 3.6.0 env-py3
```

Browse all virtual envs:
```
$ pyenv virtualenvs
  2.7.15/envs/project-py2-7-15 (created from /root/.pyenv/versions/2.7.15)
  3.6.0/envs/project-py3-6-0 (created from /root/.pyenv/versions/3.6.0)
  project-py2-7-15 (created from /root/.pyenv/versions/2.7.15)
  project-py3-6-0 (created from /root/.pyenv/versions/3.6.0)
```

Then, enter the project environment you want:
```
$ pyenv activate env-py2
(env-py2) $ <do your job>
(env-py2) $ pyenv deactivate
$
```

If you no longer need a virtual env, then delete:
```
pyenv virtualenv-delete env-py2
```

Be aware that you can install any other packages, of different versions, 
in different virtualenvs you want. 

For example, you can install Flask 0.8 in env-py2, 
and Flask 0.9 in env-py3 respectively.
