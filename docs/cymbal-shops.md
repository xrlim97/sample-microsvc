# Cymbal Shops Branding

By default, when you deploy this sample app, the "Online Boutique" branding (logo and wording) will be used.
But you may want to use Google Cloud's fictitious company, _Cymbal Shops_, instead.

To use "Cymbal Shops" branding, set the `CYMBAL_BRANDING` environment variable to `"true"` in the the Kubernetes manifest (`.yaml`) for the `frontend` Deployment.

```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: frontend
spec:
  ...
  template:
    ...
    spec:
      ...
      containers:
          ...
          env:
            ...
          - name: CYMBAL_BRANDING
            value: "true"
```

## Automated Deployment

Automated deployment for the Cymbal Shops Branding variation is now supported with [Kustomize](https://kustomize.io/). Deployment instructions can be found at [/kustomize/README.md](https://github.com/GoogleCloudPlatform/microservices-demo/blob/main/kustomize/README.md#deployment-instruction).
