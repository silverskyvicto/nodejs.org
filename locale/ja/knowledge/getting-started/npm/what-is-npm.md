---
title: npm とは?
date: '2011-08-26T10:08:50.000Z'
tags:
  - npm
difficulty: 1
layout: knowledge-post.hbs
---

<!-- 
`npm`, short for Node Package Manager, is two things: first and foremost, it is an online repository for the publishing of open-source Node.js projects; second, it is a command-line utility for interacting with said repository that aids in package installation, version management, and dependency management.  A plethora of node.js libraries and applications are published on npm, and many more are added every day. These applications can be searched for on http://search.npmjs.org/. Once you have a package you want to install, it can be installed with a single command-line command.


 -->
Node Package Manager の略である `npm` には2つの役割があります。まず第一に、オープンソースの Node.js プロジェクトを公開するためのオンラインリポジトリです。2つ目は、パッケージのインストール、バージョン管理、および依存関係管理を支援する、リポジトリと対話するためのコマンドラインユーティリティです。たくさんの Node.js ライブラリとアプリケーションが npm に公開されていて、毎日たくさん追加されています。これらのアプリケーションは http://search.npmjs.org/ で検索できます。インストールしたいパッケージを入手したら、単一のコマンドラインコマンドでインストールできます。


<!-- 
Let's say you're hard at work one day, developing the Next Great Application.  You come across a problem, and you decide that it's time to use that cool library you keep hearing about - let's use Caolan McMahon's [async](http://github.com/caolan/async) as an example. Thankfully, `npm` is very simple to use: you only have to run `npm install async`, and the specified module will be installed in the current directory under `./node_modules/`.  Once installed to your `node_modules` folder, you'll be able to use `require()` on them just like they were built-ins.

 -->
ある日あなたは仕事に苦労していて、Next Great Application を開発したとしましょう。あなたは問題に遭遇しました、そしてあなたは今聞いているそのクールなライブラリを使う時が来たと決心します - 例として Caolan McMahon の [async](http://github.com/caolan/async) を使ってみましょう。ありがたいことに、`npm` の使い方はとても簡単です: `npm install async` を実行するだけで、指定されたモジュールは `./node_modules/` の下の現在のディレクトリにインストールされます。`node_modules` フォルダにインストールされたら、それらが組み込まれているのと同じように、`require()` を使うことができます。

<!-- 
Let's look at an example of a global install - let's say `coffee-script`. The npm command is simple: `npm install coffee-script -g`. This will typically install the program and put a symlink to it in `/usr/local/bin/`.  This will then allow you to run the program from the console just like any other CLI tool.  In this case, running `coffee` will now allow you to use the coffee-script REPL.

 -->
グローバルインストールの例を見てみましょう - `coffee-script` にするとしましょう。npm コマンドは簡単です: `npm install coffee-script -g`。これは通常プログラムをインストールし、それにシンボリックリンクを `/usr/local/bin/` に置きます。これにより、他の CLI ツールと同じように、コンソールからプログラムを実行できます。この場合、`coffee` を実行すると coffee-script の REPL を使えるようになります。

<!-- 
Another important use for npm is dependency management.  When you have a node project with a [package.json](/articles/getting-started/npm/what-is-the-file-package-json) file, you can run `npm install` from the project root and npm will install all the dependencies listed in the package.json. This makes installing a Node project from a git repo much easier! For example, `vows`, one of Node's testing frameworks, can be installed from git, and its single dependency, `eyes`, can be automatically handled:

Example:

    git clone https://github.com/cloudhead/vows.git
    cd vows
    npm install

After running those commands, you will see a `node_modules` folder containing all of the project dependencies specified in the package.json.


 -->
npm のもう1つの重要な用途は依存関係管理です。[package.json](/articles/getting-started/npm/what-is-the-file-package-json) ファイルを持つ Node プロジェクトがあるときは、プロジェクトルートと npm から `npm install` を実行できます。 package.json にリストされているすべての依存関係をインストールします。これにより、git リポジトリから Node プロジェクトをインストールするのがずっと簡単になります。例えば、Node のテストフレームワークの1つである `vows` は git からインストールすることができ、その単一の依存関係 `eyes` は自動的に処理することができます。

例:

    git clone https://github.com/cloudhead/vows.git
    cd vows
    npm install

これらのコマンドを実行した後、package.json で指定されたすべてのプロジェクト依存関係を含む `node_modules` フォルダが表示されます。

