
## Initial setup

### Create and activate python virtualenv
```
$ virtualenv -p $(which python) .venv
$ . .venv/bin/activate
```

### Install required python packages
```
$ pip install -r requirements.txt
```

## Adjust system parameters ( non persistent )
```
$ sudo sysctl vm.max_map_count=262144
```

## Create ELK stack

### Execute docker-compose
```
$ docker-compose up -d
```

### Check component logs
```
$ docker-compose logs -f kib01
$ docker-compose logs -f es01
```

## Destroy ELK stack

### Execute docker-compose
```
$ docker-compose down -v
```
