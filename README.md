# Zeppelin Docker image

Zeppelin 0.7.1 docker image based on Google's Zeppelin image. 

## Run

Here you can find the most commom run configuration. 

```
docker run -d -p 0.0.0.0:8080:8080 -e ZEPPELIN_PORT=8080 -e MASTER="spark://master:7077" -t projectepic/zeppelin:latest
```

This runs on detached mode, setting spark master url, the zeppelin port and exposing it to the outside

### Ports exposable

- `8080`: Zeppelin web server
- `4040`: Spark UI web server

### Volumes available to mount

- `/opt/zeppelin/notebook/`: This is where the notebooks are stored
- `/data`
- `/home`

Check out this docker cheatsheet to add volumes or ports: [https://github.com/wsargent/docker-cheat-sheet](https://github.com/wsargent/docker-cheat-sheet)