# 01

## 基礎知識

- Unixとは

色んなOSの総称。  
LinuxはUnixを参考に作られたもので、いわゆるUnix系OSに含まれる。  
  
Unix系OSではUnixコマンドが使える。

- Unix系OS

今Unix系OSとして普及しているものは、大きく分けて**Linux**と**BSD**がある。  
Linuxの中でも多くの流派があり、Red Hat系、Debian系、Slackware系、独立系に分類することができる。  
タッチのPCに入ってるOSは、<a href="https://www.ubuntulinux.jp/">Ubuntu</a>ていうLinuxディストリビューション。

- Ubuntuについて

UbuntuはDebian系のLinuxディストリビューション。GUIでセットアップができるし、初心者に優しいこともありかなり人気で、万が一詰まっても検索すれば山ほど資料が出て来るので安心感があるOS。  
パッケージ管理システムとしてaptがある。 　
aptコマンドを使うことで簡単にソフトウェアのインストール・アンインストール等を行うことができる。  

---

## 各種基礎コマンド

### unixコマンド

#### ファイル操作系


- ディレクトリ作成  
    
```
    mkdir hoge   # hogeというディレクトリを作成 
    
    mkdir hoge1 hoge2  # このように複数ディレクトリを一度に作ることも可能    
```
        
- ディレクトリ移動  

```
    cd hoge      # hogeに移動  
       
    cd ..        # 一つ上の階層に移動  
       
    cd ~         # ホームディレクトリに移動  
```
   
- ファイル作成  
    
```
    touch hoge.txt    # hoge.txtというファイルを作成  
        
    touch hoge1.txt hoge2.txt  # このように複数ファイルを一度に作ることも可能      
```

- コピー  

```
    cp hoge.txt huga.txt   # hoge.txtというファイルをfuga.txtというファイルにコピー(fuga.txtというファイルがない場合は作成してくれる)  
    
    cp -r hoge huga        # hogeというディレクトリの中身丸ごとをhugaというディレクトリにコピー(hugaというディレクトリがない場合は作成してくれる)
```  
      
- 削除(一度消すと修復不可能)

```   
    rm hoge.txt  # hoge.txtというファイルを削除  
       
    rm *         # 自分が今いる階層の全ファイル削除  
    
    rm -r hoge   # hogeというディレクトリを削除   
```

- リネーム・移動

```
    mv hoge.txt fuga.txt    # hoge.txtをfuga.txtにリネーム  
    
    mv hoge.txt fuga        # hoge.txtをfugaというディレクトリに移動  
```

#### 確認系

- 現在地確認  

```
    pwd
```

- 現在地のファイルやディレクトリを確認

```    
    ls          # 自分がいる階層にあるファイルやディレクトリを確認  
       
    ls -a       # 隠しファイル(.ファイル)も含め自分がいる階層にあるファイルやディレクトリを確認  
```

- ファイルの中身確認

```
    cat hoge.txt    # hoge.txtの中身がコマンドラインに出力される  
    
    less hoge.txt   # hoge.txtの中身がスクロール可能な状態で閲覧できる
```

- コマンドの使い方確認

```
    man hoge    # hogeの使い方を確認
```
    
#### スーパーユーザー関連

- スーパーユーザー権限(管理者権限)で実行

```
    sudo hogehoge   # hogehgoeをスーパーユーザー権限で実行する
```

