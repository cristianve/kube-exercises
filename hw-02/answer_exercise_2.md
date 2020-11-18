Creo el objeto replicaSet con 3 replicas con el archivo nginx-rs.yaml que he creado:

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-02/images/repli.PNG)

Y ejecuto el comando:

kubectl apply -f nginx-rs.yaml

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-02/images/replicas.PNG)

Para escalar el número de replicas a 10 utilizo el siguiente comando:

kubectl scale --replicas=10 rs nginx-server

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-02/images/scale_10.PNG)

El objeto Deployment se adaptaría bien para tener una replica en cada nodo, con los tags podAntiAffinityy y podAffinity puedes 
restringir que nodos utiliza el pod.

