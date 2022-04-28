<img src="https://user-images.githubusercontent.com/6461792/165660503-26d415d7-e73c-4690-a975-bc81e6e08c79.svg" alt="drawing" width="300"/>

# Comandos Kubernetes
Uma lista com alguns comandos do Kubernets para o dia a dia :)

### Pods

Lista todos os pods do namespace atual
```sh
kubectl get pods
```

Lista todos os pods com mais detalhes
```sh
kubectl get pods -o wide
```

Informações do pod
```sh
kubectl describe pods {POD_NAME}
```

Obter o YAML|JSON de um pod
```sh
kubectl get pod {POD_NAME} -o yaml 
```
```sh
kubectl get pod {POD_NAME} -o json 
```

Deletando pod
```sh
kubectl delete pod {POD_NAME}
```

Port Forward
```sh
kubectl port-forward pod/{POD_NAME} 8000:8000
```

---

### Replicaset

Lista todos os replicasets
```sh
kubectl get replicasets
```

Escala um replicaset
```sh
kubectl scale --replicas=2 rs/{REPLICASET_NAME}
```


Escala um replicaset a partir de um yaml
```sh
kubectl scale --replicas=3 -f {FILE}
```

Deleta um replicaset
```sh
kubectl delete replicaset {REPLICASET_NAME}
```

---

### Deployment

Lista todos os deployments
```sh
kubectl get deployments
```

Informações de um deployment específico
```sh
kubectl get deployment {DEPLOYMENT_NAME}
```

Escala um deployment
```sh
kubectl scale --replicas=3 deployment/{DEPLOYMENT_NAME}
```

Escala um deployment
```sh
kubectl autoscale deployment {DEPLOYMENT_NAME} --min=2 --max=10 
```
