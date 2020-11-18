He creado el archivo deployment.yaml con las especificaciones del ejercicio 1 y con el tipo de estrategia "Recreate":

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-04/images/deploy.PNG)

Ejecuto el archivo yaml con la instrucción siguiente:

kubectl create -f deployment.yaml

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-04/images/deploy_create.PNG)

kubectl describe deployment nginx-deployment, con esta instrucción puedo ver el objeto deployment creado:

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-04/images/deploy_desc_1.PNG)

Para reaizar un rollback a la versión generada previamente utilizamos la siguiente instrucción:

kubectl rollout undo deployment.v1.apps/nginx-deployment

![alt text](https://github.com/jordill14/kube-exercises/blob/master/hw-04/images/rollout.PNG)
