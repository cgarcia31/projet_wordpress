# projet_wordpress
 Wordpress project with Kubernetes

## Step 1 : Generate a secret yaml file with the following command

      kubectl create secret generic  wordpress-mysql-secret --from-literal=wordpress=YOUR_PASSWORD -n k8s-wordpress-project --dry-run=client -o yaml >wordpress_04_secret.yaml

## Step 2 : Apply all manifests

      kubectl apply -f .

## Step 3 : Check that all objects are working

      kubectl -n k8s-wordpress-project get all

## Step 4 : Test wordpress

      Open your browser and go to http://YourMasterKubernetesServerIP:30005

## Delete all
kubectl delete -f .

You can delete the data, rm -Rf /data -> To be done on the master and the workers.
