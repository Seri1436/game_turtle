# Coding Exercise : Turtle

### Cloning the Repository

    git clone https://github.com/Seri1436/game_turtle.git


### Setting up a Virtual Environment

    cd ./game_turtle

    pyenv versions

    pyenv local 3.11.6

    python -m venv .venv
    
    source .venv/bin/activate

    pip install -r requirements.txt

### Running the Application

    python T1.py
    
### Deactivate the virtual environment

    deactivate



## No module named '_tkinter' error

Reference : [Python/Tkinter: ModuleNotFoundError: '_tkinter'](https://stackoverflow.com/questions/59987762/python-tkinter-modulenotfounderror-no-module-named-tkinter)

    아래 명령어를 실행하여 tkinter 설치 확인

    $ python -m tkinter

    만일 설치되지않았다면, 아래 명령어 실행하여 설치

    $ brew install tcl-tk
    
    $ echo 'export PATH="/usr/local/opt/tcl-tk/bin:$PATH"' >> ~/.zshrc

    $ source ~/.zshrc     # 터미널을 재시작하거나, 환경변수 재로딩

    아래 명령어를 통해, tcl-tk 가 PATH가 연결되었는지 확인

    $ echo $PATH | grep --color=auto tcl-tk

    $ export LDFLAGS="-L/usr/local/opt/tcl-tk/lib"
    $ export CPPFLAGS="-I/usr/local/opt/tcl-tk/include"
    $ export PKG_CONFIG_PATH="/usr/local/opt/tcl-tk/lib/pkgconfig"

    pyenv 에서 사용할 python 재설치

    $ pyenv versions

    $ pyenv uninstall 3.11.6

    $ pyenv install 3.11.6    # 설치하는데 시간이 꽤 걸림. 약 5분?

        python-build: use openssl@3 from homebrew
        python-build: use readline from homebrew
        Downloading Python-3.11.6.tar.xz...
        -> https://www.python.org/ftp/python/3.11.6/Python-3.11.6.tar.xz
        Installing Python-3.11.6...
        python-build: use tcl-tk from homebrew
        python-build: use readline from homebrew
        python-build: use zlib from xcode sdk

    $ pyenv local 3.11.6

    $ pyenv versions

    $ python -m venv .venv

    $ source .venv/bin/activate

    $ python -m tkinter -c "tkinter._test()"



