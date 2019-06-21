# learning-javascript-01

テクノロジー（藤原）JavaScriptの練習 (1)

## Q1の回答「コメントを解除したことで、どう変化しましたか？」

Webページを更新した時に「こんにちは！」という文字が出てきた。

## Q2の回答「エラーの原因は何でしょうか？（調べてみましょう）」

翻訳　ReferenceError：ウィンドウが定義されていません
window.alert("Hello, Node.js!!");
↑のコードの前に「// 」をつけたらエラーが出なくなった。

## Chromeデベロッパーツール：Consoleの実行結果

```
index.html:18 おはよう！
index.html:56 Live reload enabled.
Navigated to http://127.0.0.1:5500/index.html
index.html:18 おはよう！
Navigated to http://127.0.0.1:5500/index.html
index.html:18 おはよう！
Navigated to http://127.0.0.1:5500/index.html
index.html:18 おはよう！
index.html:1 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
Navigated to http://127.0.0.1:5500/index.html
index.html:18 おはよう！
index.html:1 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
Navigated to http://127.0.0.1:5500/index.html
index.html:18 おはよう！
Navigated to http://127.0.0.1:5500/index.html
index.html:18 おはよう！
index.html:52 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
socket.onmessage @ index.html:52
Navigated to http://127.0.0.1:5500/index.html
VM90 main.js:4 Good morning.
index.html:18 おはよう！
Navigated to http://127.0.0.1:5500/index.html
VM100 main.js:4 Good morning.
index.html:18 おはよう！
Navigated to http://127.0.0.1:5500/index.html
VM110 main.js:4 Good morning.
index.html:18 おはよう！
index.html:52 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
socket.onmessage @ index.html:52
Navigated to http://127.0.0.1:5500/index.html
main.js:4 Good morning.
index.html:18 おはよう！
```

## ターミナルの実行結果

```
(base) MacBook-Pro:~ nisikiakinori$ cd ~/fujiwara
(base) MacBook-Pro:fujiwara nisikiakinori$ git clone git@github.com:nishikiakinori/learning-javascript-01.git
Cloning into 'learning-javascript-01'...
remote: Enumerating objects: 10, done.
remote: Counting objects: 100% (10/10), done.
remote: Compressing objects: 100% (8/8), done.
remote: Total 10 (delta 0), reused 7 (delta 0), pack-reused 0
Receiving objects: 100% (10/10), done.
(base) MacBook-Pro:fujiwara nisikiakinori$ cd learning-javascript-01
(base) MacBook-Pro:learning-javascript-01 nisikiakinori$ code .
(base) MacBook-Pro:learning-javascript-01 nisikiakinori$ node node-main.js
-bash: node: command not found
(base) MacBook-Pro:learning-javascript-01 nisikiakinori$ node node-main.js
-bash: node: command not found
(base) MacBook-Pro:learning-javascript-01 nisikiakinori$ cat ~/.bash_profile

# Setting PATH for Python 3.7
# The original version is saved in .bash_profile.pysave
PATH="/Library/Frameworks/Python.framework/Versions/3.7/bin:${PATH}"
export PATH
# added by Anaconda3 2019.03 installer
# >>> conda init >>>
# !! Contents within this block are managed by 'conda init' !!
__conda_setup="$(CONDA_REPORT_ERRORS=false '/Users/nisikiakinori/anaconda3/bin/conda' shell.bash hook 2> /dev/null)"
if [ $? -eq 0 ]; then
    \eval "$__conda_setup"
else
    if [ -f "/Users/nisikiakinori/anaconda3/etc/profile.d/conda.sh" ]; then
        . "/Users/nisikiakinori/anaconda3/etc/profile.d/conda.sh"
        CONDA_CHANGEPS1=false conda activate base
    else
        \export PATH="/Users/nisikiakinori/anaconda3/bin:$PATH"
    fi
fi
unset __conda_setup
# <<< conda init <<<
if [ -f ~/.bashrc ]; then
  . ~/.bashrc
fi
(base) MacBook-Pro:learning-javascript-01 nisikiakinori$ 
(base) MacBook-Pro:learning-javascript-01 nisikiakinori$ echo "export PATH=$HOME/.nodebrew/current/bin:$PATH" >> ~/.bashrc
(base) MacBook-Pro:learning-javascript-01 nisikiakinori$ source ~/.bashrc
-bash: export: `Workbooks.app/Contents/SharedSupport/path-bin': not a valid identifier
(base) MacBook-Pro:learning-javascript-01 nisikiakinori$ source ~/.bashrc
-bash: export: `Workbooks.app/Contents/SharedSupport/path-bin': not a valid identifier
(base) MacBook-Pro:learning-javascript-01 nisikiakinori$ node -v
v12.4.0
(base) MacBook-Pro:learning-javascript-01 nisikiakinori$ nodeborew
-bash: nodeborew: command not found
(base) MacBook-Pro:learning-javascript-01 nisikiakinori$ nodebrew
nodebrew 1.0.1

Usage:
    nodebrew help                         Show this message
    nodebrew install <version>            Download and install <version> (from binary)
    nodebrew compile <version>            Download and install <version> (from source)
    nodebrew install-binary <version>     Alias of `install` (For backward compatibility)
    nodebrew uninstall <version>          Uninstall <version>
    nodebrew use <version>                Use <version>
    nodebrew list                         List installed versions
    nodebrew ls                           Alias for `list`
    nodebrew ls-remote                    List remote versions
    nodebrew ls-all                       List remote and installed versions
    nodebrew alias <key> <value>          Set alias
    nodebrew unalias <key>                Remove alias
    nodebrew clean <version> | all        Remove source file
    nodebrew selfupdate                   Update nodebrew
    nodebrew migrate-package <version>    Install global NPM packages contained in <version> to current version
    nodebrew exec <version> -- <command>  Execute <command> using specified <version>

Example:
    # install
    nodebrew install v8.9.4

    # use a specific version number
    nodebrew use v8.9.4
(base) MacBook-Pro:learning-javascript-01 nisikiakinori$ node node-main.js
/Users/nisikiakinori/Documents/fujiwara/learning-javascript-01/node-main.js:1
window.alert("Hello, Node.js!!");
^

ReferenceError: window is not defined
    at Object.<anonymous> (/Users/nisikiakinori/Documents/fujiwara/learning-javascript-01/node-main.js:1:1)
    at Module._compile (internal/modules/cjs/loader.js:774:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:785:10)
    at Module.load (internal/modules/cjs/loader.js:641:32)
    at Function.Module._load (internal/modules/cjs/loader.js:556:12)
    at Function.Module.runMain (internal/modules/cjs/loader.js:837:10)
    at internal/main/run_main_module.js:17:11
(base) MacBook-Pro:learning-javascript-01 nisikiakinori$ node node-main.js
(base) MacBook-Pro:learning-javascript-01 nisikiakinori$ node node-main.js
Goodmorning, Node.js!!

```

