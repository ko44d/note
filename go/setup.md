# インストール
1. goenvによる設定方法  
    ```
    $ git clone https://github.com/syndbg/goenv.git ~/.goenv
    ```
1. .zshrcに追記
    ```
    export GOENV_ROOT="$HOME/.goenv"
    export PATH="$GOENV_ROOT/bin:$PATH"
    eval "$(goenv init -)"
    ```
1. go のインストール
    ```
    ## インストールできるバージョン確認
    goenv install -l
    ## goで利用するバージョンをインストール
    goenv install 1.16.4
    ## goenvで利用するバージョンを設定
    goenv global 1.16.4
    ```
# 開発準備
1. 開発用ディレクトリ作成
    ```
    mkdir -p ~/Documents/workspace/go/src
    ```
1. GOPATH/GOBINの設定
    ```
    export GOPATH=$HOME/Documents/workspace/go/src
    export GOBIN=$GOPATH/bin
    if [ -x "`which go`" ]; then
        export PATH=$PATH:$GOBIN
    fi
    ```
    goenv の設定後に書くこと。goenv init実行時にGOPATHが上書きされてしまう。
