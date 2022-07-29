# SuiteCRM 7 Unofficial Chart
*SuiteCRM is a trademark of SalesAgility, Inc. This chart is unaffiliated with and not endorsed by SalesAgility.*
## General information
This chart deploys SuiteCRM version 7, licensed under AGPL v3. The chart can be deployed stand-alone, either with included internal or external database. 

The chart consists of a few containers. An NGINX container serves actual http(s) requests and "runs" the Angular frontend. The backend is built on top of Symfony, ie. php. The PHP is run in a PHP-FPM container. There is also an optional MariaDB container that can be enabled in values.yaml.

## License
This chart and SuiteCRM 7 are both licensed under AGPL version 3.

## Development
Pull requests are appreciated, although might not be accepted. The aim is to build a chart that can be deployed completely automatically, but other than that would be as vanilla as possible. The container image for SuiteCRM (more accurately, the php container) is built independently, see its [own repository](https://github.com/TLii/SuiteCRM7-docker).

This image has a few changes compared to the upstream SuiteCRM 7 to ease containerization. See the Docker image repository for details.

## Usage

[Helm](https://helm.sh) must be installed to use the chart.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

  helm repo add tlii-suitecrm7 [https://tlii.github.io/SuiteCRM7-chart](https://tlii.github.io/SuiteCRM7-chart/)

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
tlii-suitecrm8` to see the charts.

To install the suitecrm7 chart:

    helm install my-suitecrm7 tlii-suitecrm8/suitecrm7

To uninstall the chart:

    helm delete my-suitecrm7
