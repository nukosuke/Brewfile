# nukosuke/Brewfile
1. [Homebrew](https://brew.sh/) をインストールする
2. brew bundle
   ```sh
   $ git clone git@github.com:nukosuke/Brewfile.git
   $ cd Brewfile/
   $ brew bundle
   ```

## asdf
Homebrew でインストールした asdf に [nodejs plugin](https://github.com/asdf-vm/asdf-nodejs) を使って Node をインストールしようとすると、
`~/.asdf/lib/commands/command-help.bash: No such file or directory` のようなエラーが出ることがある。  
このスクリプトは `/usr/local/lib/commands/` にあるためシンボリックリンクを貼って対処する。

``` sh
% mkdir ~/.asdf/lib
%  ln -s /usr/local/lib/commands ~/.asdf/lib/commands
```
