To deploy the app on kubernetes use the command
kubectl apply -f .infrastructure/deployment.yml
The resources and limits for each pod are not required
Minimum number of pods is 2, and when average utilization exceeds 70%, the HPA will scale up to distribute the load.
The app continue its work even during the updates by using maxUnavailable number of pods at the same time and maxSurge for substitution for working one. 
The access to the app is the same, by ip address
127.0.0.1:8000