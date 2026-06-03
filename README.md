# dotfiles

## chezmoi

### 変更を確認する

```sh
chezmoi status
chezmoi diff
```

`status` で管理対象ファイルの差分有無を確認し、`diff` で実際の変更内容を確認します。

### ホームディレクトリ側の変更を取り込む

```sh
chezmoi add ~/.zshrc
chezmoi add ~/.npmrc
chezmoi add ~/.config/uv/uv.toml
```

### chezmoi 側の変更をホームディレクトリへ反映する

```sh
chezmoi apply
```

### chezmoi の管理ディレクトリへ移動する

```sh
chezmoi cd
```

## 参考リンク

- [chezmoi](https://www.chezmoi.io/)
- [starship](https://starship.rs/ja-JP/)
- [Nerd Fonts](https://www.nerdfonts.com/)
