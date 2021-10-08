FROM multiarch/qemu-user-static:x86_64-aarch64 as qemu
FROM arm64v8/ubuntu
COPY --from=qemu /usr/bin/qemu-ppc64le-static /usr/bin
RUN apt-get update -y
ENTRYPOINT ["/bin/cat","/proc/cpuinfo"]
