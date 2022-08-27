# Kubedoom K8S Playground

## Overview

Helm chart to run [kubedoom](https://github.com/storax/kubedoom) and serve as NodePort in K8S

Victims are using [alexwhen/docker-2048](https://github.com/alexwhen/docker-2048), but you can change to any if you want

## Config

Edit `values.yaml`

## Deploy

Use Helm
```
helm upgrade --install kubedoom-playground .

# To remove
helm uninstall kubedoom-playground
```

Or build the template and apply it manually
```
helm template > build.yaml
kubectl apply -f ./build.yaml

# To remove
kubectl delete -f ./build.yaml
```

## Play

Use [VNC Viewer](https://www.realvnc.com/en/connect/download/viewer/) and connect to the target NodePort (default to 30010)

Default password for vnc is `idbehold`. In case the game is too difficult for you, the cheat code `idkfa` can help you to get full armed
