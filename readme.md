## Steps to deploy RS and DEPLOY
    - deploy replicaSet with image nginx
    - check the pods
    - check the application
    - deploy the deployment with image nginx
    - check the pods
    - check the application

## Steps to see the difference
    - edit rs.yml with image httpd and apply
    - check the pods
    - check the application
    - scale down the pods to 0 and scale up the 3
    - check the pods
    - check the application

    - edit deploy.yml with image httpd and apply
    - check the pods
    - check the application