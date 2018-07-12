# go-k8s-mirror-image-operator

Add support mirror repository for image

### Example

```
apiVersion: extensions/v1beta1
kind: Deployment
spec:
  replicas: 1
  template:
    spec:
      containers:
        image: "{{ .Values.deployment.image.repository }}:{{ .Values.deployment.image.tag }}"
        mirrorImage:
          - URL_ONE
          - URL_TWO
          - URL_THREE
```
