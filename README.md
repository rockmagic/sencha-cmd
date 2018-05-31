# Sencha Cmd docker image for building ExtJS projects

One can pull this image using:
* version 6.5.3

  ```docker pull rockmagicnet/sencha-cmd:latest```
* version 6.2.2

  ```docker pull rockmagicnet/sencha-cmd:6.2.2```
* version 4.0.5

  ```docker pull rockmagicnet/sencha-cmd:4.0.5```
* version 4.0.1

  ```docker pull rockmagicnet/sencha-cmd:4.0.1```

## Using image for automated builds

To build app in working directory use the following command:

```
docker run --rm -v `pwd`:/app -w /app \
  rockmagicnet/sencha-cmd:latest \
  app build
```

Note that the absolute path is provided with `pwd` command.

For Sencha Cmd instructions please refer the ofiicial documentation at https://docs.sencha.com/cmd/