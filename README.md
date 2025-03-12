# gui-docker
X Display sharing dockerfile


## Setup

Allow all users access to .Xauthority, this allows ALL users read access  
Allow xhost to get connections from docker

```
echo $XAUTHORITY
chmod 644 $AUTHORITY
xhost +local:docker

```

## Running

Run it within same network directing x display to host display

```
podman run --rm -it --net=host --env DISPLAY=$DISPLAY 0x6a4b/x-gui:latest
```