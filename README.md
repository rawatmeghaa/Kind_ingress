For ingress controller 
======================

1. Install ingress controller :
   kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.10.1/deploy/static/provider/kind/deploy.yaml

   k get event -n ingress-nginx
2. Port-Forward
    k port-forward svc/ingres-controlller -n ingress-nginx 8081:80 --address 0.0.0.0 &


   curl localhost:8081/app-one
   curl localhost:801/app-two

