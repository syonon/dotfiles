# dotfiles

個人用の dotfiles を [chezmoi](https://www.chezmoi.io/) で管理するリポジトリです。

## chezmoi の軽い使い方

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

普段どおりホームディレクトリ上の設定ファイルを編集したあと、`chezmoi add` で chezmoi の管理元に反映します。

### chezmoi 側の変更をホームディレクトリへ反映する

```sh
chezmoi apply
```

リポジトリ側で編集した内容を実際のホームディレクトリへ適用します。

### chezmoi の管理ディレクトリへ移動する

```sh
chezmoi cd
```

このリポジトリの管理元ディレクトリへ移動します。移動後は通常の Git リポジトリとして扱えます。

```sh
git status
git add .
git commit -m "Update dotfiles"
git push
```

### 新しい環境でセットアップする

```sh
chezmoi init --apply https://github.com/syonon/dotfiles.git
```

private リポジトリなので、事前に GitHub へ認証できる状態にしておきます。

## 管理中のファイル

- `~/.zshrc`
- `~/.npmrc`
- `~/.config/uv/uv.toml`

## 参考リンク

- [chezmoi 公式サイト](https://www.chezmoi.io/)
- [Quick start](https://www.chezmoi.io/quick-start/)
- [User guide: setup](https://www.chezmoi.io/user-guide/setup/)
- [User guide: daily operations](https://www.chezmoi.io/user-guide/daily-operations/)
- [Command overview](https://www.chezmoi.io/user-guide/command-overview/)
- [Commands reference](https://www.chezmoi.io/reference/commands/)
