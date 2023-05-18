
# Fork the `lemonade-supply` repository


Browse to the workshop group's Lemonade Supply project at
[`https://gitlab.com/eastside-kubernetes-workshop/lemonade-supply`](https://gitlab.com/eastside-kubernetes-workshop/lemonade-supply)
On the right side will be a button for `Fork`.

Press the `Fork` button and then choose the new group you just
created from the list of namespaces. When you choose a namespace
the project is forked/copied into your group. 

# Clone the repository to your local system

Use `git clone` to create a copy of the `lemonade-supply` on your
local computer.

# Update the `k8s/config` file in the `lemonade-supply` repository

Just like in the `cup-supply` repository, the `k8s/config` file in the
`lemonade-supply` repository contains the definition of your cluster
and most importantly two key pieces of information.

You can copy this file directly from the `cup-supply` project you
just setup. Probably this command works:

```
cp ../cup-supply/k8s/config ./k8s/
```

# Commit the changes to the `cup-supply` repository

```
git commit -am "Updated Kubernetes configuration file."
git push
```

# Check the pipeline to for successful completion

After the `git push` the job should succeed. Check for errors. 

