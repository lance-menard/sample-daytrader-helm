# sample.daytrader.microservices Helm Chart

This repo contains a Helm chart that can be used to deploy [Sample Daytrader Microservices](https://github.com/sample-daytrader/sample.daytrader.microservices) onto a supported Kubernetes cluster.

## Using the Chart

### Pushing images

If, like me, the build command in the main sample.daytrader.microservices repositories failed to push images due to an auth error, you can use `docker login` in a shell combined with the `./scripts/push-images.sh` script to easily push new images to the `srlpr` account.

### Installation

Once access to the Kubernetes cluster is configured, run `./scripts/install-daytrader.sh`.

### Updating

To update the helm chart or running images, make any changes required to the templates and run `./scripts/upgrade-daytrader.sh`.

### Uninstalling

To uninstall the application, run `./scripts/uninstall-daytrader.sh`.

### Running

Once installed, run `./scripts/port-forward.sh` to forward the daytrader application to http://localhost:8080.
