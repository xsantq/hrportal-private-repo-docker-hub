# hrportal-private-repo-docker-hub

In k8s pulling image from private repository in docker hub.

- sample deployment yaml included
- ın k8s a secret is needed for docker hub authentication. Use following command:

      kubectl create secret docker-registry docker-hub-secret --docker-username <username> --docker-password=<password> --docker-email= <your@mail.com>
- In deployment.yaml put this in the container spec part:

         imagePullSecrets:
         - name: docker-hub-secret
     

