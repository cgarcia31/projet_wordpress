# projet_wordpress
 Wordpress project with Kubernetes

## Step 1 : Generate a secret yaml file with the following command

 - kubectl create secret generic  wordpress-mysql-secret --from-literal=wordpress=YourPassword -n k8s-wordpress-project --dry-run=client -o yaml >wordpress_03_secret.yaml

## Step 2 : Replace the name of the storage class with your own for the following files :

      - wordpress_02_pvc_mysql.yaml
      - wordpress_06_pvc_web_data.yaml

## Step 3 : Apply all manifests

kubectl apply -f .

## Step 4 : Check that all objects are working

kubectl -n k8s-wordpress-project get all

## Step 5 : Test wordpress

Open your browser and go to http://YourMasterKubernetesServerIP:30005
