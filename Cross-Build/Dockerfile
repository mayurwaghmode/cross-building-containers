FROM docker.io/multiarch/qemu-user-static as qemu
FROM docker.io/ppc64le/ubuntu:20.04
COPY --from=qemu /usr/bin/qemu-ppc64le-static /usr/bin
RUN apt-get update -y
ENTRYPOINT ["/bin/cat","/proc/cpuinfo"]
