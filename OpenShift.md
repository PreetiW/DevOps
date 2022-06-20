# OpenShift CLI (oc)

### Most used commands
----

* **oc login -u USER_NAME or oc login <token_copied_from_cluster>:**
This commands helps in log in to the OpenShift CLI (oc) to access and manage your cluster.

* **oc process:**
Process a template into list of resources

For eg:
```
  # Process a file locally instead of contacting the server
  oc process -f template.json --local -o yaml
```

* **oc apply:**
Apply a configuration to a resource by filename or stdin

For eg:
```
  # Apply the JSON passed into stdin to a pod.
  cat pod.json | oc apply -f -
```

* **oc port-forward:**
Forward one or more local ports to a pod

For eg:
```
# Listen on port 8888 locally, forwarding to 5000 in the pod
  oc port-forward pod/mypod 8888:5000

# Listen on ports 5000 and 6000 locally, forwarding data to/from ports 5000 and 6000 in the pod
  oc port-forward pod/mypod 5000 6000  
```


---

Note: also check [bonfire](https://github.com/RedHatInsights/bonfire), a CLI tool w.r.t RedHat Insights