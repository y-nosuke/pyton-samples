# pyton-samples

## Pythonインストール

``` shell
pip install pyenv-win --target $HOME\\.pyenv

[System.Environment]::SetEnvironmentVariable('PYENV',$env:USERPROFILE + "\.pyenv\pyenv-win\","User")
[System.Environment]::SetEnvironmentVariable('PYENV_ROOT',$env:USERPROFILE + "\.pyenv\pyenv-win\","User")
[System.Environment]::SetEnvironmentVariable('PYENV_HOME',$env:USERPROFILE + "\.pyenv\pyenv-win\","User")

[System.Environment]::SetEnvironmentVariable('path', $env:USERPROFILE + "\.pyenv\pyenv-win\bin;" + $env:USERPROFILE + "\.pyenv\pyenv-win\shims;" + [System.Environment]::GetEnvironmentVariable('path', "User"),"User")
```

``` shell
(Invoke-WebRequest -Uri https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py -UseBasicParsing).Content | python -
[System.Environment]::SetEnvironmentVariable('path', $env:USERPROFILE + "\.poetry\bin;" + [System.Environment]::GetEnvironmentVariable('path', "User"),"User")
```

``` shell
poetry new プロジェクト名
cd プロジェクト名
poetry install

pyenv install --list
pyenv install 3.9.6
pyenv local 3.9.6
python --version
python -m venv venv
. ./venv/Scripts/activate
```

## 参考

- [Visual Studio Code（VSCode）とPython](https://zenn.dev/tfukumori/articles/4c46bc78774871)
- [pyenv + venvを使ったpython仮想環境（Windows向け）](https://qiita.com/HyunwookPark/items/9f46524b69da75d3fba3)
- [Poetry documentation](https://cocoatomo.github.io/poetry-ja/)
