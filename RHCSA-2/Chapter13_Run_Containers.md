# 13.03 Creating Containers with podman #

* By default the containers run in foreground mode if we want the container to run in background we have to use `-d` option along with `podman run`.
* We can delete the images with `podman rmi` command.
* `podman run -d --name web1 --rm -p 8081:8080 <image-name>` with this command we are going to create a container with the name `web1` with the port 8081 in the host and foward to 8080 in the container and with the option --rm we are going to redeploy the container if exist already.
* `podman exec -it <image-id|container-name> sh` run a shell of a container.
* `podman run -e <Variable-name>` we can use the option `-e` to specifiy a enviroment variable to the container.
* `podman pull <image-name>` fetch a image 

# 13.05 Registries #

* `/etc/containers/registries.conf` file contains the registries that podman search for fetch images
* `{XDG_RUNTIME_DIR}/containers/auth.json` store the password of podman authenticated registries.

# 13.07 containers lifecycle #

* `podman kill <container-name|id>` stop container forcefully
* `podman rm -f <id|container-name>` remove forcefully a container if is running
* `podman generate systemd --new --files --name webapp` 
* `systemctl --user daemon-reload`
* `loginctl enable-linger` keep the service in the user context [systemctl --user] running even when the user is not loging.
* 