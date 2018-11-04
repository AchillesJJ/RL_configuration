# RL_configuration
configuration for RL task on Linux OS (Deepin OS)

## 系统安装git
    sudo apt-get install git

## 安装python版本管理器pyenv
#### git下载pyenv仓库并配置bashrc文件
    git clone git://github.com/yyuu/pyenv.git ~/.pyenv
    vim ~/.bashrc
    # 在bashrc末尾加入以下语句
    export PYENV_ROOT="$HOME/.pyenv"
    export PATH="$PYENV_ROOT/bin:$PATH"
    eval "$(pyenv init -)"
    # 在命令行运行
    source ~/.bashrc

#### 安装pyenv所需依赖库
    sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev \
    libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
    xz-utils tk-dev libffi-dev liblzma-dev
    # 安装完成后，在命令行输入pyenv，可确认是否安装成功

## pyenv下载python3
    pyenv install 3.6.5
    # 将全局python版本设置为3.6.5，pyenv versions可查看全部已有版本
    pyenv global 3.6.5

## pip安装常用库
    pip3 install numpy
    pip3 install pandas
    pip3 install matplotlib
    pip3 install tensorflow
    pip3 install keras
    pip3 install scikit-learn

## 安装技术分析库TA-Lib
#### 下载依赖库
登入链接[ta-lib link](https://sourceforge.net/projects/ta-lib/)下载压缩文件，并解压执行以下命令
    
    tar -zxvf ta-lib-0.4.0-src.tar.gz
    cd ta-lib-0.4.0
    ./configure --prefix=/usr
    make
    sudo make install
#### 安装TA-Lib
    pip3 install TA-Lib

## 安装代码编辑器，推荐Atom
Atom 下载链接[atom-editor](https://atom.io/), 选择debian安装包安装即可
