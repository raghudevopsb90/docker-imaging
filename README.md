# docker-imaging

One folder per Dockerfile instruction. Every example is Nginx on `redhat/ubi10`.

Go in order. Each folder only uses instructions from the folders before it.

| Folder | Instruction |
|---|---|
| 01-FROM | FROM |
| 02-RUN | RUN |
| 03-CMD | CMD |
| 04-ENTRYPOINT | ENTRYPOINT (with CMD as arguments) |
| 05-EXPOSE | EXPOSE |
| 06-COPY | COPY |
| 07-ADD | ADD (local archive and URL) |
| 08-WORKDIR | WORKDIR |
| 09-ENV | ENV |
| 10-ARG | ARG |
| 11-LABEL | LABEL |
| 12-USER | USER |
| 13-VOLUME | VOLUME |
| 14-HEALTHCHECK | HEALTHCHECK |
| 15-STOPSIGNAL | STOPSIGNAL |
| 16-SHELL | SHELL |
| 17-ONBUILD | ONBUILD (build `base` first, then `app`) |
| 18-MULTI-STAGE | FROM ... AS and COPY --from |

## Build and run

```bash
cd 06-COPY
docker build -t nginx-copy .
docker run -d --name nginx-copy -p 8080:80 nginx-copy
curl localhost:8080
docker rm -f nginx-copy
```

ONBUILD needs the base image first:

```bash
docker build -t nginx-onbuild-base 17-ONBUILD/base
docker build -t nginx-onbuild-app 17-ONBUILD/app
```
