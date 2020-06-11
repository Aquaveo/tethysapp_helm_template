# Tethys Charts Repo
This repository contains the helm chart for Tethysapp templates. These charts are designed for use by Tethys apps, and has not been tested for usability in stand-alone mode.

### How to install
This Github page is currently being build from the /docs folder in the master branch. The helm charts are located here.

To add this repo, you can run this command
```console
helm repo add tethysapp https://aquaveo.github.io/tethysapp_helm_template/
```

To use this library, you need to add it in your requirements.yaml file inside your tethys app helm folder. Inside your requirements.txt should look like this:
``` console
dependencies:
  - name: tethysapp
    version: 0.1.0
    repository: "https://aquaveo.github.io/tethysapp_helm_template/"
```

The following files from your app helm templates needs to be updated:
+ deployment.yaml (with the following content)
  + {{- include "tethysapp.deployment" . }}   
+ ingress.yaml (with the following content)
  + {{- include "tethysapp.ingress" . }}   
+ pvc.yaml (with the following content)
  + {{- include "tethysapp.pvc" . }}   
+ service.yaml (with the following content)
  + {{- include "tethysapp.service" . }}

You can also use the values.yaml files in this repo as a starting point for your values.yaml in the app.         