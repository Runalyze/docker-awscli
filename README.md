# docker-awscli

![Docker Pulls](https://img.shields.io/docker/pulls/banst/awscli.svg?label=pulls&logo=docker&style=flat-square)
![MicroBadger Size](https://img.shields.io/microbadger/image-size/banst/awscli.svg?style=flat-square)

awscli in a container

```shell
docker run --rm -it banst/awscli --version
```

This image is [automatically builded](https://github.com/BastienAr/docker-awscli/actions) every 6 hours if there is a new release available from aws official repository.

As this image is mainly useful in a CI context, [jq](https://stedolan.github.io/jq/) is also provided in it, to parse some awscli response.

```shell
aws apigateway get-rest-apis | jq -r '.items[]|select(.name == "my-api")|.id'
```
