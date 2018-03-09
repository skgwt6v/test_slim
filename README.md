# セットアップ手順
+ anyenvのインストール
+ rbenvのインストール
+ bundlerのインストール
+ gemのインストール

## 1 anyenvのインストール
```
$ git clone https://github.com/riywo/anyenv ~/.anyenv
$ echo 'export PATH="$HOME/.anyenv/bin:$PATH"' >> ~/.bash_profile
$ echo 'eval "$(anyenv init -)"' >> ~/.bash_profile
$ exec $SHELL -l 
```

## 2 rbenvのインストール

```
$ anyenb rbenv
$ rbenv install  2.4.1
$ rbenv global  2.4.1

# ruby-buildを入れて、rbenvのバージョンごとに環境を構築
$ git clone https://github.com/sstephenson/ruby-build.git  ~/.anyenv/envs/rbenv/plugins/ruby-build 

```

## 3 bundlerのインストール

```
$ rbenv exec gem install bundler
$ rbenv rehash
$ echo 'export PATH="$HOME/.anyenv/envs/rbenv/versions/2.4.1/bin:$PATH"' >> ~/.bash_profile
```

## 4 gemのインストール

```
# gemをインストール
$ bundle install
```