# openresty-gip-check-container

コンテナ環境から出ていくGIPをシュッと確認したいとき用のやつ

Cloud RunとかでNAT IP固定成功してるかなーとか見たいときに使った

## how to build

```shell
docker build --rm -t openresty-gip -f ./docker/Dockerfile .
```

## how to debug

```shell
docker run -p 80:80 -itd openresty-gip
curl http://localhost/
-> <return GIP>
```

## how to use

Cloud Runとかに80で動くようにデプロイしてそのエンドポイントを見るだけ
