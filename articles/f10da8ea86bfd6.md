---
title: "中級Git操作、第2回"
emoji: "👋"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: []
published: false
---
### リベース

- git commit --fixup=<commit> + git rebase --autosquash
- git rebase --update-refsとstacking branches
    - git config --global rebase.updateRefs true

## でかいレポジトリ用

- git config --global fetch.writeCommitGraph true
- git config core.fsmonitor true -> でかいレポジトリでもgit statusが素早くなる
- git clone --filter=blob:none
- git clone --filter=tree:0
- scalarで巨大なレポジトリに対するデフォルトを設定
- git-lfs

- time git log --graph --oneline -10 >> /dev/null
- git sparse checkout
- git ls-remote -> PRにレフがあるので、？？？
- git submodulesの導入は間違いだった

Part 2

- フック共有：pre-commitとhusky
- .gitattributes
    - exiftoolで画像の（メタデータの）diffを有効化
    - git-lfs
- worktreesで複数のブランチで同時作業
