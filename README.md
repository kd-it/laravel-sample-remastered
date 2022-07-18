# このリポジトリについて

このリポジトリは、AS構築Ⅰ(2022年度)のDockerを用いたLaravel環境構築の流れを再現するためのものです。
概ね授業メモの状況に添って作っています。

# 使い方

メモ(10)〜(13)の内容を追いかけたい人は、初期状態からの推移を見ることをお勧めします。

PS> docker compose build
PS> docker compose up -d

確認中にチェックアウトをした場合、内容とイメージがかち合わないことが想定されるので、適宜rebuild/restartが必要になるので注意してください。

## 注意

Laravelプロジェクト作成後の状態を使うとき、まだ必要なモジュールが入ってない可能性が十分に高いので、composerを使ってインストールしてあげてください。

```
PS> docker compose up -d
# frontend内のcomposerを読んで、package.json/lockに従ってのモジュールインストールを行う
PS> docker compose exec frontend composer install
```


# ざっくり時系列

1. メモ(10)
    1. 初期のdocker-compose環境
    2. Laravelプロジェクトの作成
