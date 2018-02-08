# Run OpenMapKitServer on Hasura.io

## What does this come with?

* OpenMapKitServer
* Deployed with node server
* **Dockerfile** (automatically used by Hasura for deployment)

## How to run

* Install Hasura CLI https://docs.hasura.io/0.15/manual/install-hasura-cli.html
* Clone this repository in your computer
* Create a cluster with `hasura cluster create --type free`
* Get the id of your created cluster and edit the file `clusters.yaml`, replacing `canon50` by your cluster id
* Add the remote hasura repository with `git remote add hasura ssh://hasura@<your_cluster_id>.hasura-app.io:22/~/git/<your_cluster_id>/`
* Deploy with `git push hasura master`
