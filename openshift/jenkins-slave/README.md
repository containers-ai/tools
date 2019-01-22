# Pushing Application Images to an External Registry
- CREATE A NEW PROJECT
```console
oc new-project YOUR-PROJECT
```

- SETUP DOCKER CREDENTIALS AS A SECRET
```console
oc create secret generic dockerhub --from-file=config.json
```

- ADD SECRET TO YOUR BUILDER SERVICE ACCOUNT
```console
oc edit sa builder
```

- EDIT BUILDCONFIG TO PUSH TO YOUR DOCKER REGISTRY
```console
oc new-build https://github.com/containers-ai/tools.git --context-dir=openshift/jenkins-slave/go -o yaml > jenkins-slave-go.yaml
# Edit jenkins-slave-go.yaml
oc create -f jenkins-slave-go.yaml
```

[Reference](https://blog.openshift.com/pushing-application-images-to-an-external-registry/)
