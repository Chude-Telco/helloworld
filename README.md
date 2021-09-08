# helloworld


vagrant@kubemaster:~/kubernetes-engine-samples/hello-app/manifests$ curl http://10.100.80.165:8080
Hello, world!
Version: 2.0.0
Hostname: helloweb-67c794d6df-mr2fh
vagrant@kubemaster:~/kubernetes-engine-samples/hello-app/manifests$ kubectl describe ingress helloweb
Name:             helloweb
Namespace:        default
Address:
Default backend:  helloweb-backend:8080 (10.44.0.1:8080)
Rules:
  Host        Path  Backends
  ----        ----  --------
  *           *     helloweb-backend:8080 (10.44.0.1:8080)
Annotations:  kubernetes.io/ingress.global-static-ip-name: helloweb-ip
Events:       <none>
vagrant@kubemaster:~/kubernetes-engine-samples/hello-app/manifests$ curl http://10.44.0.1:8080
Hello, world!
Version: 2.0.0
Hostname: helloweb-67c794d6df-mr2fh
vagrant@kubemaster:~/kubernetes-engine-samples/hello-app/manifests$
