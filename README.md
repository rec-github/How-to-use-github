# Github基本のキ
Githubの基本を簡単にまとめる。

## ブラウザからの操作まとめ

### リポジトリの作成
Repositoriesを開き、画面右上あたりのNewをクリックし、タイトル等を設定する。

### README.mdの更新方法
README.mdの右端のペンのマークをクリックすると編集画面に入れる。  

’#’の個数が多いほど文字のサイズが小さい見出しとなる。  

’#’のと見出しの間にはスペースを１つ入力する必要がある。  

\`\`\`言語名  
内容  
\`\`\`  
と入力すると言語名に対応した表示をしてくれる。  

ページ下部の"Commit Change"をクリックすると更新が反映される。  

### Issuesについて
Issueを開き、画面右上あたりのNew Issueをクリックする。  
タイトルを設定する。  
Codeを開き新しいBranchを生成する。この時、生成したbranchのタイトルの末尾に/#"Issueの末尾についている番号"をつけるとPull requestsした際に、対応するIssueにいつ更新したかという情報が追加される。
masterに直接書くのではなく新しいbranchを更新し、masterにPull requestsするとバックアップのようなものを作ることができる。（ハッシュ値を利用） 
完了したIssueは当該Issueを開いたときのページ下部にあるClose issueをクリックすると完了したことがわかりやすい。

### Pull requestsについて
Pull requestsを開きNew pull requestsをクリック。  
baseに更新先のbranch、compareに更新元のbranchを置く。  
Create pull requestsをクリック。  
もう一度Create pull requestsをクリック。  
Merge pull requestをクリック。  
Confilm mergeをクリック。  
完了。

## コンソールからの操作まとめ

### 下準備
PCにgithub用のディレクトリを作成する。  
そのディレクトリに移動し、  
git clone "リポジトリのURL"  
と入力する。  
(リポジトリのURLはCodeページのClone or downloadをクリックすると表示されるURLのことである。)  
すると、ディレクトリ内にリポジトリ名と同名のディレクトリが作成されるので移動する。  
この中のファイルを操作する。  
初回は  
git config --global user.email "メールアドレス"  
git config --global user.name "ユーザ名"  
を実行しておく必要がある。（エラーメッセージで丁寧に教えてくれる。）  

### ブラウザでの更新内容をディレクトリに反映させる方法
リポジトリに対応するディレクトリ内で、  
git pull  
を実行すると反映される。

### ファイルの更新
エディタで既存のファイルを更新した後、  
git add -u  
と入力し、続いて  
git commit -m "コメント"  
git push  
と入力することで、更新内容がgithubに反映される。  
新規ファイルを作成した場合は  
git add "ファイル名"  
と入力する必要がある。

### 操作するbranchの変更
現在ディレクトリが参照しているbranchの調べ方は、  
git branch  
を実行すればよい。\*がついているbranchが参照中のブランチである。  
branchの変更をする場合は  
git checkout "branch名"  
を実行すればよい。

