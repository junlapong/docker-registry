# Private Docker Registry

## Setup

1. TLS Certificate (TBD)
2. Add User

```
docker run -i --rm --entrypoint htpasswd registry \
    -Bbn docker tcuser >> config/auth/htpasswd
```

## Run

```
# START
docker-compose up -d

# VIEW LOGS
docker-compose logs -f

# STOP
docker-compose logs -f
```

## Testing

- http://localhost:5000/v2/_catalog

```json
{
    "repositories": []
}
```

- Setup docker client
- Test docker push

## References
- [docker registry on docker hub](https://hub.docker.com/_/registry)
- [maxmasetti/docker-compose-registry](https://github.com/maxmasetti/docker-compose-registry)
- [Quiq/docker-registry-ui](https://github.com/Quiq/docker-registry-ui)
- [ทำ Private Registry เก็บ images docker ไว้ใช้เอง](https://medium.com/@nprch_12/%E0%B8%97%E0%B8%B3-private-registry-%E0%B9%80%E0%B8%81%E0%B9%87%E0%B8%9A-images-docker-%E0%B9%84%E0%B8%A7%E0%B9%89%E0%B9%83%E0%B8%8A%E0%B9%89%E0%B9%80%E0%B8%AD%E0%B8%87-20470475cdb8)
