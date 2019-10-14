# Sencha Cmd docker image for building ExtJS projects

One can pull this image using:
* version 7.0.0

  ```docker pull rockmagicnet/sencha-cmd:latest```

  or 

  ```docker pull rockmagicnet/sencha-cmd:7.0.0```

* version 6.7.0

  ```docker pull rockmagicnet/sencha-cmd:6.7.0```

* version 6.6.0

  ```docker pull rockmagicnet/sencha-cmd:6.6.0```

* version 6.5.3

  ```docker pull rockmagicnet/sencha-cmd:6.5.3```
* version 6.2.2

  ```docker pull rockmagicnet/sencha-cmd:6.2.2```
* version 5.1.3

  ```docker pull rockmagicnet/sencha-cmd:5.1.3```
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

For Sencha Cmd instructions please refer the official documentation at https://docs.sencha.com/cmd/