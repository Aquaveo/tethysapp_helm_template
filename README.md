# Tethys Charts Repo
This repository contains the helm chart for Tethysapp templates. These charts are designed for use by Tethys apps, and has not been tested for usability in stand-alone mode.

### How to install
This Github page is currently being build from the /docs folder in the master branch. The helm charts are located here.

To add this repo, you can run this command
```console
helm repo add tethysapp https://aquaveo.github.io/tethysapp_helm_template/
```

You can search what is inside this repo:
```console
helm search repo tethysapp
```
You should see these following charts:
``` console
NAME                            CHART VERSION   APP VERSION     DESCRIPTION     
misc-helm-chart/geoserver       0.1.12          latest          Geoserver       
misc-helm-chart/postgis         0.1.12          latest          PostGIS Database
```

Run this command to install:
``` console
helm install misc-helm-chart/geoserver --generate-name
```