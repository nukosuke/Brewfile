# nukosuke/Brewfile
1. [Homebrew](https://brew.sh/) をインストールする
2. brew bundle
   ```sh
   $ git clone git@github.com:nukosuke/Brewfile.git
   $ cd Brewfile/
   $ brew bundle
   ```

## dotfiles を配置
[nukosuke/dotfiles](https://github.com/nukosuke/dotfiles) を `git clone` しシンボリックリンクを貼る。

``` sh
% git clone git@github.com:nukosuke/dotfiles.git
% cd dotfiles/
# 確認
% ./dotfiles.pl dry_link
# 実行
% ./dotfiles.pl link
```

## AquaSKK
- ツールバーのIMEメニューから `キーボード環境設定を開く` を選択し、入力ソースに `AquaSKK統合` を追加する
- メニューに追加された `AquaSKK -> 環境設定` を選択

### 拡張設定
以下のように設定。

| 有効 | 拡張設定規則                             | 区分     |
|:-----|------------------------------------------|----------|
| x    | 拡張ローマ字入力「AZIK」を使う(US配列用) | システム |

### 辞書
以下のように設定。

| 有効 | 辞書の種類                 | 場所           |
|:-----|----------------------------|----------------|
| x    | SKK 辞書(UTF-8)            | `~/.skk-jisyo` |
| x    | SKK 辞書(自動ダウンロード) | `SKK-JISYO.L`  |

## asdf
Homebrew でインストールした asdf に [nodejs plugin](https://github.com/asdf-vm/asdf-nodejs) を使って Node をインストールしようとすると、
`~/.asdf/lib/commands/command-help.bash: No such file or directory` のようなエラーが出ることがある。  
このスクリプトは `/usr/local/lib/commands/` にあるためシンボリックリンクを貼って対処する。

``` sh
% mkdir ~/.asdf/lib
%  ln -s /usr/local/lib/commands ~/.asdf/lib/commands
```

## Emacs
[nukosuke/.emacs.d](https://github.com/nukosuke/.emacs.d) を `git clone` して配置。

``` sh
% git clone git@github.com:nukosuke/.emacs.d.git .config/emacs
```
