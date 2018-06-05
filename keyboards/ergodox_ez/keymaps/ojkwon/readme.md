This folder contains custom keymap for my own based on ergodox ez default.

To build, refer
https://github.com/kwonoj/qmk_firmware/blob/master/docs/getting_started_build_tools.md#docker

```sh
export DOCKER_IMAGE_TAG=${tagname}
docker build -t $DOCKER_IMAGE .
./util/docker_build.sh ergodox_ez:ojkwon

ls ./.build
```

// Deprecated,
TL:DR, under root of qmk
build image via `docker -t ${dockerImageTag} .`
then `docker run -e keymap=ojkwon -e keyboard=ergodox_ez --rm -v $('pwd'):/qmk:rw ${dockerImageTag}`