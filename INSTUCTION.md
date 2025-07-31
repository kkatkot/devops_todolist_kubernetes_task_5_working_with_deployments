To deploy the app on kubernetes use the command
kubectl apply -f deployment.yml
The resources for each pod are not defined
The minimux number of pods is 2. When the load on the pods exceed 70%, the controller automatically create new one to diverse the load.
The app continue its work even during the updates by using maxUnavailable number of pods at the same time and maxSurge for substitution for working one. 
The access to the app is the same, by ip address
127.0.0.1:8000