# gitcm

emoji prefix commit message generator :sunglasses:

## options

| option   | commit message                    | English description                                                                                    | Japanese description                   |
| -------- | --------------------------------- | ------------------------------------------------------------------------------------------------------ | -------------------------------------- |
| create   | `🌱create: your_commit_message`   | create a new file                                                                                      | 新規ファイル作成                       |
| feat     | `✨feat: your_commit_message`     | A new feature                                                                                          | 新しい機能                             |
| fix      | `🐛fix: your_commit_message`      | A bug fix                                                                                              | バグの修正                             |
| docs     | `📝docs: your_commit_message`     | Documentation only changes                                                                             | ドキュメントのみの変更                 |
| style    | `💄style: your_commit_message`    | Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc) | 空白、フォーマット、セミコロン追加など |
| refactor | `♻️refactor: your_commit_message` | A code change that neither fixes a bug nor adds a feature                                              | 仕様に影響がないコード改善             |
| perf     | `⚡️perf: your_commit_message`    | A code change that improves performance                                                                | パフォーマンス向上のコード改善         |
| test     | `🚨test: your_commit_message`     | Adding missing or correcting existing tests                                                            | テスト追加、修正                       |
| chore    | `🔧chore: your_commit_message`    | Changes to the build process or auxiliary tools and libraries such as documentation generation         | ビルド、補助ツール、ライブラリ関連     |
| none     | `your_commit_message`             | No prefix                                                                                              | 接頭辞なしでコミット                   |

## Usage

example:

```sh
$ gitcm feat "add new feature"
```

then commit message will be:  
![commit-message-on-github](https://user-images.githubusercontent.com/63878044/163709738-40bd9464-9e33-4962-bb54-b99be97fc208.png)

## Install

If you use Windows , you have to use -DWIN option at compile time.

```sh
$ git clone https://github.com/shebang-sh/gitcm.git
$ cd gitcm

# For UNIX like OS
$ gcc gitcm.c -o gitcm
$ mkdir -p $HOME/.local/bin
$ cp gitcm $HOME/.local/bin/gitcm
$ echo '\nalias gitcm=$HOME/.local/bin/gitcm' >> $HOME/.zshrc # or .bashrc
$ source $HOME/.zshrc # or .bashrc

# For Windows
$ gcc gitcm.c -o gitcm.exe -DWIN # for Windows
$ mkdir -p $HOME\local\bin
$ Copy-Item -Path .\gitcm.exe -Destination "$HOME\local\bin\gitcm.exe"
$ echo '`r`nSet-Alias gitcm "$HOME\local\bin\gitcm.exe"' >> $profile
$ . $profile
```

### 参考

1. [僕が考える最強のコミットメッセージの書き方](https://qiita.com/konatsu_p/items/dfe199ebe3a7d2010b3e)
2. [GitHub のコミットメッセージに絵文字を入れて開発効率をあげる](https://qiita.com/Jung0/items/0a9a7a97a2c17f92d3c5)
