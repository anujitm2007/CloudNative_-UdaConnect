vagrant@anuj-machine:~/my-work/CloudNative_-UdaConnect/deployment$ kubectl create -f .
configmap/db-env created
secret/db-secret created
persistentvolume/postgres-volume created
persistentvolumeclaim/postgres-pv-claim created
service/postgres created
deployment.apps/postgres created
service/udaconnect-api created
deployment.apps/udaconnect-api created
service/udaconnect-app created
deployment.apps/udaconnect-app created
vagrant@anuj-machine:~/my-work/CloudNative_-UdaConnect/deployment$ kubectl get po
NAME                              READY   STATUS    RESTARTS   AGE
postgres-5f676c995d-mdl9s         1/1     Running   0          13s
udaconnect-api-89dbffbf9-2qltg    1/1     Running   0          13s
udaconnect-app-6ddf7c79fb-9rxt2   1/1     Running   0          13s
vagrant@anuj-machine:~/my-work/CloudNative_-UdaConnect/deployment$ kubectl get svc
NAME             TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)          AGE
kubernetes       ClusterIP   10.43.0.1       <none>        443/TCP          64d
postgres         NodePort    10.43.160.164   <none>        5432:30841/TCP   24s
udaconnect-api   NodePort    10.43.43.151    <none>        5000:30001/TCP   24s
udaconnect-app   NodePort    10.43.220.222   <none>        3000:30000/TCP   24s
