# Udagram API - Users Service

A part of [Udagram App](https://github.com/Sasa94s/udagram-app) project, in fulfillment of Udacity's Cloud Developer Nanodegree.

## Getting Started

To run this service separately, build the docker image:
```shell
docker build -t udagram-api-users-service .
```
Run the container:
```shell
docker run \
-e POSTGRES_USERNAME=postgres  \
-e POSTGRES_PASSWORD=totallynotmypassword \
-e POSTGRES_HOST=database.ctxaw5xe1d4f.eu-west-2.rds.amazonaws.com \
-e POSTGRES_DB=udagram \
-e AWS_BUCKET=k8s-udagram-bucket \
-e AWS_REGION=eu-west-2 \
-e AWS_PROFILE=default \
-e JWT_SECRET=helloworld \
-e URL=http://localhost:8080 \
-e PORT=8200 \
-p 8200:8200 udagram-api-users-service
```
