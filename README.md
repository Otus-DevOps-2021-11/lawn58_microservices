# lawn58_microservices
lawn58 microservices repository

###ДЗ Docker контейнеры###

Создан образ из Dockerfile  
Cоздан контейнер из образа  
Образ запушен в  DockerHub  


docker run cadb35fb6709/otus_reddit:latest  

###ДЗ Docker образы. Микросервисы###

основы написания Dockerfile;  
основные команды используемые при написание Dockerfile;  
базовые образы;  
микросервисы  

###ДЗ Сетевое взаимодействие Docker контейнеров. Docker Compose. Тестирование образов###  

Узнали/научились  
Docker compose  
Docker networks  

###ДЗ Логирование приложений###

Научились в ELK и Zipking

###ДЗ Kubernetes###

Мини методичка по тому, как работать с kubernetes и одним подом на винде

minikube  --- инструмент для запуска одноузлового кластера Kubernetes на виртуальной машине в персональном компьютере


kubectl   --- Инструмент командной строки Kubernetes kubectl позволяет запускать команды для кластеров Kubernetes


C:\Users\<USER>\.kube\config   - конфиг kubectl

C:\Users\<USER>\.minikube\machines\minikube    - файлы ISO и остальные для создания VM

root:без пароля
docker:tcuser

kubectl get nodes    - информация о нодах(серверах) в кластере
kubectl cluster-info - показать информацию о кластере

minikube start --vm-driver=virtualbox  - запуск кластера на linux/macOS
minikube start -p MYCLUSTER  - запуск кластера c нашим именем
minikube stop	  - остановка
minikube delete   - удаление


minikube start --cous=4 --memory=8gb --disk-size=25gb


minikube ssh  - зайти под юзером docker


-------

kubectl run hello --image=adv4000/k8sphp:latest --port=80    - запускаем контейнер из image и пробрасываем 80 порт

kubectl delete pods hello hello1

kubectl describe pods hello   - подробная информация о поде (контейнере)

kubectl exec hello date   - выполнить команду date в поде(контейнере) hello
kubectl exec -it hello sh - зайти в контейнер под рутом 
kubectl logs hello        - вывести логи пода (контейнера)
kubectl port-forward hello 7788:80  - перенаправить 80 порт контейнера на 7788 свой порт

kubectl apply -f pod-myweb-ver1.yaml  - запускаем приложение из манифеста
kubectl delete  -f pod-myweb-ver1.yaml  - удаляем под


###Основные модели безопасности и контроллеры в Kubernetes###

Научились поднимать kubernetes кластер в yandex cloud
