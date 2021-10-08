FROM docker.io/multiarch/qemu-user-static as qemu
FROM docker.io/arm64v8/ubuntu
COPY --from=qemu /usr/bin/qemu-aarch64-static /usr/bin
RUN apt-get update -y
ENTRYPOINT ["/bin/cat","/proc/cpuinfo"]
