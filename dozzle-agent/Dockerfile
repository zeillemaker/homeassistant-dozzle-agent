FROM amir20/dozzle:v8.4.1 AS dozzle

FROM alpine:3.14 AS base

# Create a symlink from /run/docker.sock to /var/run/docker.sock
RUN ln -s /run/docker.sock /var/run/docker.sock

COPY --from=dozzle /dozzle /dozzle

EXPOSE 7007

ENTRYPOINT ["/dozzle", "agent"]