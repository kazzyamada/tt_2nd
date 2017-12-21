# https://qiita.com/ay3/items/8d758ebde41d256a32dc
# GitHub 入門

$ git config user.email kazz.yamada@gmail.com
$ git config user.name kazzyamada
$ git config --list
filter.media.required=true
filter.media.clean=git media clean %f
filter.media.smudge=git media smudge %f
user.name=kazzyamada
user.email=kazz.yamada@gmai.com
filter.hawser.clean=git hawser clean %f
filter.hawser.smudge=git hawser smudge %f
filter.hawser.required=true
push.default=matching
alias.co=checkout
credential.helper=osxkeychain
core.bare=false
core.filemode=true
core.ignorecase=true
core.precomposeunicode=true
core.logallrefupdates=true
core.repositoryformatversion=0
remote.origin.url=https://github.com/kazzyamada/tt_2nd.git
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*

$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	.README.md.swp

no changes added to commit (use "git add" and/or "git commit -a")



$ git init
Reinitialized existing Git repository in /Users/season/GitHub/tt_2nd/.git/

$ git add README.md

$ git commit -m "first commit"
[master (root-commit) 947d17f] first commit
 1 file changed, 8 insertions(+)
 create mode 100644 README.md

$ git remote add origin https://github.com/kazzyamada/tt_2nd.git

$ git push -u origin master
remote: Repository not found.
fatal: repository 'https://github.com/kazzyamada/tt_2nd.git/' not found



# origin 登録
# https://github.com/kazzyamada/tt_2nd.git に「origin」というあだ名をつけるようなイメージ。

$ git remote add origin https://github.com/kazzyamada/tt_2nd.git

ユーザ名やパスワードを聞かれるので入力。
origin は共有リポジトリのこと。レポジトリの場所(URL)の別名。
master はブランチ（枝分かれ）の名前。ちなみに master は大事なブランチなので、個人利用では自由にpushしても大丈夫だけど、チームでの場合はmasterには通常pushしないので注意。ブランチはGUIから確認可能（<>Codeタブのすぐ下に n branches と出ていて、クリックすると詳細が見れる）。

$ git push -u origin master
remote: Repository not found.
fatal: repository 'https://github.com/kazzyamada/tt_2nd.git/' not found

$ git remote -v
origin	https://github.com/kazzyamada/tt_2nd.git (fetch)
origin	https://github.com/kazzyamada/tt_2nd.git (push)


