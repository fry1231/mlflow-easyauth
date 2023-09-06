
# mlflow with basic auth

Standard [mlflow](https://mlflow.org/) does not have any authentication for the web-interface.
This project adds basic HTTP authentication with a single username, password to the web interface and API.
And packages this up in a easy-to-install Docker image.


## License
[Licensed](./LICENSE.txt) under Apache 2.0, as mlflow itself.

## Status

**In Use**

# Quickstart

## Run with Docker

Clone this git repo

```
git clone https://github.com/fry1231/mlflow-easyauth.git
cd mlflow-easyauth
```

Fill in user credentials in a .env file

```bash
MLFLOW_TRACKING_USERNAME=
MLFLOW_TRACKING_PASSWORD=
```

Build and run the image

```
docker compose --env-file .env up -d --build
```

```

## Use in mlflow client

Configure the client

    export MLFLOW_TRACKING_URI=http://localhost:8001
    export MLFLOW_TRACKING_USERNAME=user
    export MLFLOW_TRACKING_PASSWORD=pass

Run some code using the mlflow tracking API. There is an example included in this repo

    export MLFLOW_EXPERIMENT_NAME=test6
    python3 example.py

Open the web browser and go to your deployed .
You should now have runs tracked with metrics being logged.

For more details see official documentation on
[mlflow tracking integration](https://www.mlflow.org/docs/latest/quickstart.html#using-the-tracking-api).

# Configuration options

All configuration is done as environment variables.
Set them using the preferred method for your Docker host.

