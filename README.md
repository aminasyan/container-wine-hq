# container-wine-hq
Containerize Wine HQ to run on RHEL/podman
After building container run it as below for Windows GUI applications
```
podman run --userns keep-id -it --tz local --device=/dev/dri -e HOME -e DISPLAY -e XDG_RUNTIME_DIR -e XAUTHORITY -e WINEPREFIX -v $HOME/.wine:$HOME/.wine -v $HOME/.cache:$HOME/.cache -v $XDG_RUNTIME_DIR:$XDG_RUNTIME_DIR --net=host container-wine-hq:latest 
```

