Creo el pod con las especificaciones de forma declarativa con el archivo pod.yaml que he creado:

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-01/images/pod_yaml.PNG)

Y ejecuto el comando:

kubectl create -f pod.yaml

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-01/images/run_pod.PNG)

Para obtener las últimas 10 líneas ejecuto el siguiente comando:

kubectl logs nginx-server --tail 10

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-01/images/logs.PNG)

Para obtener la IP interna del pod ejecuto el siguiente comando:

kubectl describe pod nginx-server | grep IP | sed -E 's/IP:[[:space:]]+//'

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-01/images/pod_ip.PNG)

Para entrar en el pod ejecuto el siguiente comando:

kubectl exec -it nginx-server -- bash

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-01/images/inside_pod.PNG)

Una vez dentro del pod, para visualizar el contenido de NGINX ejecuto el siguiente comando:

cat docker-entrypoint.sh

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-01/images/contenido_imagen.PNG)

La calidad de servicio (QoS) será Guaranteed, ya que la reuqests y los límites establecidos por el archivo pod.yaml son iguales.


![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-01/images/qos.PNG)
