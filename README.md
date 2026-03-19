### Домашнее задание к занятию «Базовые объекты K8S»# kuber-homeworks.
### Цель задания:

В тестовой среде для работы с Kubernetes, установленной в предыдущем ДЗ, необходимо развернуть Pod с приложением и подключиться к нему со своего локального компьютера.

### Чеклист готовности к домашнему заданию:

1.Установленное k8s-решение (например, MicroK8S).

2.Установленный локальный kubectl.

3.Редактор YAML-файлов с подключенным Git-репозиторием.

### Задание 1. Создать Pod с именем hello-world.

1.Создать манифест (yaml-конфигурацию) Pod.

2.Использовать image - gcr.io/kubernetes-e2e-test-images/echoserver:2.2.

3.Подключиться локально к Pod с помощью kubectl port-forward и вывести значение (curl или в браузере).

### Ответ.
Команды:

kubectl apply -f manifests/hello-world-pod.yaml

kubectl get pods

kubectl port-forward pod/hello-world 8080:8080

http://localhost:8080
<img width="1337" height="638" alt="дз1" src="https://github.com/user-attachments/assets/767e4aa3-f4f3-4c49-9d53-665f4c5e44ef" />

### Задание 2. Создать Service и подключить его к Pod.

1.Создать Pod с именем netology-web.

2.Использовать image — gcr.io/kubernetes-e2e-test-images/echoserver:2.2.

3.Создать Service с именем netology-svc и подключить к netology-web.

4.Подключиться локально к Service с помощью kubectl port-forward и вывести значение (curl или в браузере).

### Ответ.
Команды:

apply -f manifests/netology-web.yaml

kubectl get pods

kubectl get svc

kubectl port-forward svc/netology-svc 8080:8080

curl http://localhost:8080

<img width="1442" height="540" alt="дз2" src="https://github.com/user-attachments/assets/e6f69589-64b0-4cb8-a860-f67382d7abcc" />

