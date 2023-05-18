# Fork The Cup Supply Project

Our first step is to fork the cup supply. We could create the Kubernetes
cluster first, but to save a few cents we hold of building the cluster
until the first services is ready to deploy. If you want start with 
the cluster follow the instructions in the [`ClusterSetup.md`](ClusterSetup.md)
document, then return here.

# Now fork the project

Browse to the workshop group's Cup Supply project at
[`https://gitlab.com/eastside-kubernetes-workshop/cup-supply`](https://gitlab.com/eastside-kubernetes-workshop/cup-supply)
On the right side will be a button for `Fork`.

Press the `Fork` button and then choose the new group you just
created from the list of namespaces. When you choose a namespace
the project is forked/copied into your group. 

# Build your copy of the Cup Supply project

On the left side menu, click on `CI / CD`. In the sub menu that pops up
choose `Pipelines`. 

Click on the button for 'Run Pipeline'. Leave blank any fields. At this
point we don't have information for the variables we need to create. 

This pipeline will run the *build* and *package* steps, but the *deploy* 
step will fail. That's okay for now.

# Done, return to the ReadMe

Return back to the [`README.md`](README.md#create-a-kubernetes-cluster-and-setup-the-namespace) file now, and 
continue on to create your cluster. 


