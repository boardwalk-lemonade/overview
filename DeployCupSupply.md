

# Clone a copy to your local system

You have already forked the repository to a GitLab project group in
your account. 

Now use `git clone` to create a copy on your local computer.

# Update the `k8s/config` file in the `cup-supply` repository

The `k8s/config` file in the cup-supply repository contains the
definition of your cluster and most importantly two key pieces of
information.  The are the api endpoint for the cluster and the
cluster's certificate.  All data going to or from the specifiec api
endpoint will be encrypted with the public key found in the the
cluster's certificate.

This config is needed when GitLab CI runs `kubectl` from the
`.gitlab-ci.yaml` file in the deployment stage.

The lines you need are found in your Kubernetes configuration file
which is found in your home directory in the `.kube` folder in the
`config` file. The lines you need to copy from your `~/.kube/config`
file are:

```
apiVersion: v1
clusters:
- cluster:
    certificate-authority-data: <really long line of base64 configuration date>
    server: <your servers ip address>
  name: <your servers name>
contexts:
- name:  <your servers name>
  context:
    cluster: <your servers name>
current-context: <your servers name>
kind: Config
```

# Commit the changes to the `cup-supply` repository

```
git commit -am "Updated Kubernetes configuration file."
git push
```

# Check the pipeline to for successful completion

After the `git push` the job should succeed. Check for errors. 

A likely error that we ran into on the first `kubctl` command. The
error `Unable to connect to the server: net/http: invalid header field
value "Bearer: . . . `. In this case you probaly have a newline or
other white space on the end of the value fro the `KUBE_TOKEN`

