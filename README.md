- role
  - app
    - git pull & restart
  - nginx
    - cp & restart
  - tools
    - alp
    - cp Makefile
      - nginx slow query log

## コマンドメモ

### alp

```
# 事前準備
sudo truncate -s 0 -c /var/log/nginx/access.log
top

# ベンチマーカー実行

# 実行後
sudo cat /var/log/nginx/access.log | alp ltsv -m "/api/isu/[0-9a-zA-Z]+,/api/condition/[0-9a-zA-Z]+,/api/[0-9a-zA-Z]+,/api/[0-9a-zA-Z]+/graph" --sort avg -r
make slow-show
```