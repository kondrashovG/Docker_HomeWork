### Сборка образа

```
docker build ./ --tag stock_pr
```

### Запуск контейнера

```
docker run --name my_stockpr -d -p 8000:8000 stock_pr
```
