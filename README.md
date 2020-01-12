# docker-ansible-handson

dockerコンテナをansibleでプロビジョニングするサンプル。

LAMP環境を構築し、その上でWordPressを実行します。


## リポジトリ構成

```sh
./
├── README.md
├── docker-compose.yml
├── ansible
│   ├── Dockerfile
│   └── data # ansible playbook を配置するディレクトリ
├── db
│   └── Dockerfile
└── web
    └── Dockerfile
```

## Usage

git clone

```
git clone https://github.com/s-yoshiki/docker-ansible-handson.git
cd docker-ansible-handson
```

コンテナ起動

```
docker-compose up -d
docker-compose exec ansible /bin/bash
```

ansible playbook実行

```
cd /var/data
ansible-playbook -i inventry.ini site-web.yml
```

WordPress確認

http://localhost:8080