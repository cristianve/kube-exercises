He creado los 3 yaml de tipo Service con las especificaciones:

- Exponiendo el servicio al exterior:

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-03/images/svc_ext.PNG)

kubectl create -f service1.yaml

- De forma interna:

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-03/images/svc_int.PNG)

kubectl create -f service2.yaml

- Abriendo puerto específico:

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-03/images/svc_espec.PNG)

kubectl create -f service3.yaml

Ejecutamos cada yml y vemos los objectos service para la aplicación del ejercicio anterior:

kubectl get svc

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-03/images/svc_all.PNG)


