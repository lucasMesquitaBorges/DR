Last login: Wed Nov  3 10:15:25 on console
santiagopaschoalick@FBSP-TECH-0365 ~ % docker ps
CONTAINER ID   IMAGE                    COMMAND           CREATED        STATUS              PORTS                                      NAMES
29444f8fdc3e   rancher/rancher:latest   "entrypoint.sh"   42 hours ago   Up About a minute   0.0.0.0:80->80/tcp, 0.0.0.0:443->443/tcp   awesome_feistel
santiagopaschoalick@FBSP-TECH-0365 ~ % docker stop 29444f8fdc3e
29444f8fdc3e
santiagopaschoalick@FBSP-TECH-0365 ~ % 
santiagopaschoalick@FBSP-TECH-0365 ~ % 
santiagopaschoalick@FBSP-TECH-0365 ~ % 
santiagopaschoalick@FBSP-TECH-0365 ~ % cd
santiagopaschoalick@FBSP-TECH-0365 ~ % cd .kube 
santiagopaschoalick@FBSP-TECH-0365 .kube % ls
CL1		LOCAL		PROD-02		cache
CLT01		MEU		RANCHERSERVER	config
DEV		PROD-01		TOOLS		plugins
santiagopaschoalick@FBSP-TECH-0365 .kube % cp TOOLS config 
santiagopaschoalick@FBSP-TECH-0365 .kube % kubectl get -n defectdojo ingress
Warning: extensions/v1beta1 Ingress is deprecated in v1.14+, unavailable in v1.22+; use networking.k8s.io/v1 Ingress
NAME         CLASS    HOSTS                         ADDRESS   PORTS   AGE
defectdojo   <none>   defectdojo.fretebras.tec.br             80      54s
santiagopaschoalick@FBSP-TECH-0365 .kube % kubectl get -n defectdojo ingress
Warning: extensions/v1beta1 Ingress is deprecated in v1.14+, unavailable in v1.22+; use networking.k8s.io/v1 Ingress
NAME         CLASS    HOSTS                         ADDRESS                                                                         PORTS   AGE
defectdojo   <none>   defectdojo.fretebras.tec.br   abcdd55e6c44941cd9d16f7940a8614d-c7bacfab8df81588.elb.us-east-1.amazonaws.com   80      64s
santiagopaschoalick@FBSP-TECH-0365 .kube % kubectl get -n defectdojo ingress
Warning: extensions/v1beta1 Ingress is deprecated in v1.14+, unavailable in v1.22+; use networking.k8s.io/v1 Ingress
No resources found in defectdojo namespace.
santiagopaschoalick@FBSP-TECH-0365 .kube % CD
santiagopaschoalick@FBSP-TECH-0365 .kube % cd 
santiagopaschoalick@FBSP-TECH-0365 ~ % cd Projetos 
santiagopaschoalick@FBSP-TECH-0365 Projetos % 
santiagopaschoalick@FBSP-TECH-0365 Projetos % 
santiagopaschoalick@FBSP-TECH-0365 Projetos % 
santiagopaschoalick@FBSP-TECH-0365 Projetos % clear

santiagopaschoalick@FBSP-TECH-0365 Projetos % ls
AGENDA			EXPORT			MONGO-DUMP		OWASP			RUNDECK			django-DefectDojo
AUTOSCALE		GIT			MONGO-GUI		PERCONA			SAVEMONEY		kubeless
CLOUDFLARE		GRAFANA			MONGODB			POSTGRES		SECUREBOX		rundeck.yaml
CRON			HELLO-KUBERNETES	MONGODB-SANDBOX		POSTGRES-LOCALHOST	TOWER			tmp_velero
DEV			KAFKA			MSSQL			POSTGRES2		VELERO			virtmanager
DNS			KONG			MYSQL-OPERATOR		PROXYSQL		WORDPRESS
DOKUWIKI		KONG-LOCAL		NGINX-WEB		RANCHER			WORDPRESS2
DR			KONGA			NODERED			RANCHER-SINGLEINSTANCE	autoterraform
EASY			KUBERMETRICS		ODOO			REDIS			awx
ELASTICSEARCH		MEU			OPENSEARCH		REDIS-OPERATOR		devspace
santiagopaschoalick@FBSP-TECH-0365 Projetos % cd KONG
santiagopaschoalick@FBSP-TECH-0365 KONG % ls
PopulaBancoKong		deployment.yaml		ingress-prod01.yaml	service-admin.yaml	service-kong.yaml
daemonset.yaml		docker-compose.yml	ingress.yaml		service-internal.yaml	service.yaml
santiagopaschoalick@FBSP-TECH-0365 KONG % nano service-internal.yaml 
santiagopaschoalick@FBSP-TECH-0365 KONG % 
santiagopaschoalick@FBSP-TECH-0365 KONG % 
santiagopaschoalick@FBSP-TECH-0365 KONG % cp service-internal.yaml ../django-DefectDojo 
santiagopaschoalick@FBSP-TECH-0365 KONG % cd ..
santiagopaschoalick@FBSP-TECH-0365 Projetos % cd django-DefectDojo 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % ls
Dockerfile.django				docker-compose.override.debug.yml		manage.py
Dockerfile.integration-tests			docker-compose.override.dev.yml			nginx
Dockerfile.nginx				docker-compose.override.https.yml		readme-docs
LICENSE.md					docker-compose.override.integration_tests.yml	requirements.txt
README.md					docker-compose.override.unit_tests.yml		service-internal.yaml
SECURITY.md					docker-compose.override.unit_tests_cicd.yml	setup
_config.yml					docker-compose.yml				temp.json
app.json					docs						tests
components					dojo						wsgi.py
ct.yaml						helm						wsgi_params
docker						kubeless.json
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % nano service-internal.yaml 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % nano service-internal.yaml
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % nano service-internal.yaml
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % nano service-internal.yaml
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % nano service-internal.yaml
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl -n defectdojo apply -f service-internal.yaml  
service/defectdojo-internal created
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl get -n defectdojo svc
NAME                             TYPE           CLUSTER-IP       EXTERNAL-IP                                                                       PORT(S)                                 AGE
defectdojo-django                ClusterIP      172.20.195.67    <none>                                                                            80/TCP                                  11h
defectdojo-internal              LoadBalancer   172.20.138.44    internal-abb73392c9e9e4d12a1d63e4a70b54d3-371472199.us-east-1.elb.amazonaws.com   443:31377/TCP,80:32499/TCP              12s
defectdojo-postgresql            ClusterIP      172.20.230.26    <none>                                                                            5432/TCP                                11h
defectdojo-postgresql-headless   ClusterIP      None             <none>                                                                            5432/TCP                                11h
defectdojo-rabbitmq              ClusterIP      172.20.164.183   <none>                                                                            5672/TCP,4369/TCP,25672/TCP,15672/TCP   11h
defectdojo-rabbitmq-headless     ClusterIP      None             <none>                                                                            4369/TCP,5672/TCP,25672/TCP,15672/TCP   11h
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % nano service-internal.yaml                           
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % nano service-internal.yaml
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl -n defectdojo apply -f service-internal.yaml 
service/defectdojo-internal configured
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % nano service-internal.yaml                           
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl -n defectdojo apply -f service-internal.yaml 
service/defectdojo-internal configured
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl get -n defectdojo svc
NAME                             TYPE           CLUSTER-IP       EXTERNAL-IP                                                                       PORT(S)                                 AGE
defectdojo-django                ClusterIP      172.20.195.67    <none>                                                                            80/TCP                                  12h
defectdojo-internal              LoadBalancer   172.20.138.44    internal-abb73392c9e9e4d12a1d63e4a70b54d3-371472199.us-east-1.elb.amazonaws.com   8080:32385/TCP                          71m
defectdojo-postgresql            ClusterIP      172.20.230.26    <none>                                                                            5432/TCP                                12h
defectdojo-postgresql-headless   ClusterIP      None             <none>                                                                            5432/TCP                                12h
defectdojo-rabbitmq              ClusterIP      172.20.164.183   <none>                                                                            5672/TCP,4369/TCP,25672/TCP,15672/TCP   12h
defectdojo-rabbitmq-headless     ClusterIP      None             <none>                                                                            4369/TCP,5672/TCP,25672/TCP,15672/TCP   12h
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % nano service-internal.yaml                           
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl -n defectdojo apply -f service-internal.yaml 
service/defectdojo-internal configured
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl port-forward --namespace=defectdojo service/defectdojo-django 8080:80 
Forwarding from 127.0.0.1:8080 -> 8080
Forwarding from [::1]:8080 -> 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
^C%                                                                                                                                                         santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl port-forward --namespace=defectdojo service/defectdojo-django 80:80  
Unable to listen on port 80: Listeners failed to create with the following errors: [unable to create listener: Error listen tcp4 127.0.0.1:80: bind: permission denied unable to create listener: Error listen tcp6 [::1]:80: bind: permission denied]
error: unable to listen on any of the requested ports: [{80 8080}]
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % telnet localhost 80
Trying ::1...
telnet: connect to address ::1: Connection refused
Trying 127.0.0.1...
telnet: connect to address 127.0.0.1: Connection refused
telnet: Unable to connect to remote host
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl port-forward --namespace=defectdojo service/defectdojo-django 80   
Unable to listen on port 80: Listeners failed to create with the following errors: [unable to create listener: Error listen tcp4 127.0.0.1:80: bind: permission denied unable to create listener: Error listen tcp6 [::1]:80: bind: permission denied]
error: unable to listen on any of the requested ports: [{80 8080}]
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl port-forward --namespace=defectdojo service/defectdojo-django 8080:8080
error: Service defectdojo-django does not have a service port 8080
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl port-forward --namespace=defectdojo service/defectdojo-django 8080:80  
Forwarding from 127.0.0.1:8080 -> 8080
Forwarding from [::1]:8080 -> 8080
Handling connection for 8080
Handling connection for 8080
^C%                                                                                                                                                         santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl -n defectdojo delete -f service-internal.yaml 
service "defectdojo-internal" deleted



santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl port-forward --namespace=defectdojo service/defectdojo-django 8080:80
Forwarding from 127.0.0.1:8080 -> 8080
Forwarding from [::1]:8080 -> 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
^[[AHandling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
^[[A^[[AHandling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
^[[A^[[AHandling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080


^C%                                                                                                                                                         santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % echo $DJANGO_INGRESS_ENABLED

santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % echo $DJANGO_INGRESS_ENABLED                                                 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % echo $DJANGO_INGRESS_ACTIVATE_TLS

santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % DJANGO_INGRESS_ENABLED=false
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % echo DJANGO_INGRESS_ENABLED      
DJANGO_INGRESS_ENABLED
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % echo $DJANGO_INGRESS_ENABLED
false
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % DJANGO_INGRESS_ACTIVATE_TLS=false
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % clear\
> 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % clear

santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % helm uninstall -n defectdojo defectdojo
helm install \
  defectdojo \
  ./helm/defectdojo \
  --set django.ingress.enabled=${DJANGO_INGRESS_ENABLED} \
  --set django.ingress.activateTLS=${DJANGO_INGRESS_ACTIVATE_TLS}
WARNING: Kubernetes configuration file is group-readable. This is insecure. Location: /Users/santiagopaschoalick/.kube/config
WARNING: Kubernetes configuration file is world-readable. This is insecure. Location: /Users/santiagopaschoalick/.kube/config
release "defectdojo" uninstalled
WARNING: Kubernetes configuration file is group-readable. This is insecure. Location: /Users/santiagopaschoalick/.kube/config
WARNING: Kubernetes configuration file is world-readable. This is insecure. Location: /Users/santiagopaschoalick/.kube/config
NAME: defectdojo
LAST DEPLOYED: Wed Nov  3 12:53:17 2021
NAMESPACE: default
STATUS: deployed
REVISION: 1
NOTES:
DefectDojo has been installed.

To be able to access it, set up an ingress or access the service directly by
running the following command:

    kubectl port-forward --namespace=default \
      service/defectdojo-django 8080:80

As you set your host value to defectdojo.default.minikube.local, make sure that it resolves to
the localhost IP address, e.g. by adding the following two lines to /etc/hosts:

    ::1       defectdojo.default.minikube.local
    127.0.0.1 defectdojo.default.minikube.local

To access DefectDojo, go to <http://defectdojo.default.minikube.local:8080>.

Log in with username admin.
To find out the password, run the following command:

    echo "DefectDojo admin password: $(kubectl \
      get secret defectdojo \
      --namespace=default \
      --output jsonpath='{.data.DD_ADMIN_PASSWORD}' \
      | base64 --decode)"
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % ls
Dockerfile.django				docker-compose.override.debug.yml		manage.py
Dockerfile.integration-tests			docker-compose.override.dev.yml			nginx
Dockerfile.nginx				docker-compose.override.https.yml		readme-docs
LICENSE.md					docker-compose.override.integration_tests.yml	requirements.txt
README.md					docker-compose.override.unit_tests.yml		service-internal.yaml
SECURITY.md					docker-compose.override.unit_tests_cicd.yml	setup
_config.yml					docker-compose.yml				temp.json
app.json					docs						tests
components					dojo						wsgi.py
ct.yaml						helm						wsgi_params
docker						kubeless.json
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % pwd
/Users/santiagopaschoalick/Projetos/django-DefectDojo
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % clear

santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % ls
Dockerfile.django				docker-compose.override.debug.yml		manage.py
Dockerfile.integration-tests			docker-compose.override.dev.yml			nginx
Dockerfile.nginx				docker-compose.override.https.yml		readme-docs
LICENSE.md					docker-compose.override.integration_tests.yml	requirements.txt
README.md					docker-compose.override.unit_tests.yml		service-internal.yaml
SECURITY.md					docker-compose.override.unit_tests_cicd.yml	setup
_config.yml					docker-compose.yml				temp.json
app.json					docs						tests
components					dojo						wsgi.py
ct.yaml						helm						wsgi_params
docker						kubeless.json
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % helm install -n defectdojo defectdojo \
  ./helm/defectdojo \
  --set django.ingress.enabled=${DJANGO_INGRESS_ENABLED} \
  --set django.ingress.activateTLS=${DJANGO_INGRESS_ACTIVATE_TLS} \
  --set createSecret=true \
  --set createRedisSecret=true \
  --set createMysqlSecret=true \
  --set host="defectdojo.fretebras.tec.br  
dquote> 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % helm install -n defectdojo defectdojo \
  ./helm/defectdojo \
  --set django.ingress.enabled=${DJANGO_INGRESS_ENABLED} \
  --set django.ingress.activateTLS=${DJANGO_INGRESS_ACTIVATE_TLS} \
  --set createSecret=true \
  --set createRedisSecret=true \
  --set createMysqlSecret=true \
  --set host="defectdojo.fretebras.tec.br"
WARNING: Kubernetes configuration file is group-readable. This is insecure. Location: /Users/santiagopaschoalick/.kube/config
WARNING: Kubernetes configuration file is world-readable. This is insecure. Location: /Users/santiagopaschoalick/.kube/config
NAME: defectdojo
LAST DEPLOYED: Wed Nov  3 13:03:49 2021
NAMESPACE: defectdojo
STATUS: deployed
REVISION: 1
NOTES:
DefectDojo has been installed.

To be able to access it, set up an ingress or access the service directly by
running the following command:

    kubectl port-forward --namespace=defectdojo \
      service/defectdojo-django 8080:80

As you set your host value to defectdojo.fretebras.tec.br, make sure that it resolves to
the localhost IP address, e.g. by adding the following two lines to /etc/hosts:

    ::1       defectdojo.fretebras.tec.br
    127.0.0.1 defectdojo.fretebras.tec.br

To access DefectDojo, go to <http://defectdojo.fretebras.tec.br:8080>.

Log in with username admin.
To find out the password, run the following command:

    echo "DefectDojo admin password: $(kubectl \
      get secret defectdojo \
      --namespace=defectdojo \
      --output jsonpath='{.data.DD_ADMIN_PASSWORD}' \
      | base64 --decode)"
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl port-forward --namespace=defectdojo service/defectdojo-django 8080:80
Forwarding from 127.0.0.1:8080 -> 8080
Forwarding from [::1]:8080 -> 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
Handling connection for 8080
^C%                                                                                                                                                         santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl get -n defectdojo svc
NAME                             TYPE           CLUSTER-IP       EXTERNAL-IP                                                                       PORT(S)                                 AGE
defectdojo-django                ClusterIP      172.20.186.11    <none>                                                                            80/TCP                                  11m
defectdojo-internal              LoadBalancer   172.20.165.159   internal-a4bef362a3ae54f2ea23b5c518c68c36-874790797.us-east-1.elb.amazonaws.com   443:32056/TCP,80:31263/TCP              2m8s
defectdojo-postgresql            ClusterIP      172.20.178.34    <none>                                                                            5432/TCP                                11m
defectdojo-postgresql-headless   ClusterIP      None             <none>                                                                            5432/TCP                                11m
defectdojo-rabbitmq              ClusterIP      172.20.248.80    <none>                                                                            5672/TCP,4369/TCP,25672/TCP,15672/TCP   11m
defectdojo-rabbitmq-headless     ClusterIP      None             <none>                                                                            4369/TCP,5672/TCP,25672/TCP,15672/TCP   11m
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % ping defectdojo.fretebras.tec.br
PING internal-a4bef362a3ae54f2ea23b5c518c68c36-874790797.us-east-1.elb.amazonaws.com (10.81.10.56): 56 data bytes
Request timeout for icmp_seq 0
Request timeout for icmp_seq 1
Request timeout for icmp_seq 2
Request timeout for icmp_seq 3
Request timeout for icmp_seq 4
Request timeout for icmp_seq 5
Request timeout for icmp_seq 6
Request timeout for icmp_seq 7
Request timeout for icmp_seq 8
Request timeout for icmp_seq 9
Request timeout for icmp_seq 10
Request timeout for icmp_seq 11
Request timeout for icmp_seq 12
Request timeout for icmp_seq 13
Request timeout for icmp_seq 14
Request timeout for icmp_seq 15
Request timeout for icmp_seq 16
Request timeout for icmp_seq 17
Request timeout for icmp_seq 18
Request timeout for icmp_seq 19
Request timeout for icmp_seq 20
^C
--- internal-a4bef362a3ae54f2ea23b5c518c68c36-874790797.us-east-1.elb.amazonaws.com ping statistics ---
22 packets transmitted, 0 packets received, 100.0% packet loss
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % helm install -n defectdojo defectdojo \                                      
  ./helm/defectdojo \
  --set django.ingress.enabled=${DJANGO_INGRESS_ENABLED} \
  --set django.ingress.activateTLS=${DJANGO_INGRESS_ACTIVATE_TLS} \
  --set createSecret=true \
  --set createRedisSecret=true \
  --set createMysqlSecret=true \
  --set host="defectdojo.fretebras.tec.br 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % helm install -n defectdojo defectdojo \                                      
  ./helm/defectdojo \
  --set django.ingress.enabled=${DJANGO_INGRESS_ENABLED} \
  --set django.ingress.activateTLS=${DJANGO_INGRESS_ACTIVATE_TLS} \
  --set createSecret=true \
  --set createRedisSecret=true \
  --set createMysqlSecret=true \
  --set host="defectdojo.fretebras.tec.br"
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % ping defectdojo.fretebras.tec.br
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % echo "DefectDojo admin password: $(kubectl -n defectdojo \
  get secret defectdojo \
  --namespace=default \
  --output jsonpath='{.data.DD_ADMIN_PASSWORD}' \
  | base64 --decode)"
Error from server (NotFound): secrets "defectdojo" not found
DefectDojo admin password: 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % echo "DefectDojo admin password: $(kubectl \              
  get secret defectdojo \
  --namespace=defectdojo \
  --output jsonpath='{.data.DD_ADMIN_PASSWORD}' \
  | base64 --decode)"
DefectDojo admin password: z3U97lZ7m5f81oH9cSmT7K
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % clear

santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl get ingress
Warning: extensions/v1beta1 Ingress is deprecated in v1.14+, unavailable in v1.22+; use networking.k8s.io/v1 Ingress
No resources found in default namespace.
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl -n ingress get ingress
Warning: extensions/v1beta1 Ingress is deprecated in v1.14+, unavailable in v1.22+; use networking.k8s.io/v1 Ingress
No resources found in ingress namespace.
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl get -n ingress ingress
Warning: extensions/v1beta1 Ingress is deprecated in v1.14+, unavailable in v1.22+; use networking.k8s.io/v1 Ingress
No resources found in ingress namespace.
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl get -n ingress        
You must specify the type of resource to get. Use "kubectl api-resources" for a complete list of supported resources.

error: Required resource not specified.
Use "kubectl explain <resource>" for a detailed description of that resource (e.g. kubectl explain pods).
See 'kubectl get -h' for help and examples
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl get -n ingress svc
NAME    TYPE           CLUSTER-IP      EXTERNAL-IP                                                                     PORT(S)                      AGE
tools   LoadBalancer   172.20.144.92   abcdd55e6c44941cd9d16f7940a8614d-c7bacfab8df81588.elb.us-east-1.amazonaws.com   443:31982/TCP,80:32197/TCP   183d
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl edit -n ingress tools
error: the server doesn't have a resource type "tools"
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % kubectl edit -n ingress svc tools
Edit cancelled, no changes made.
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % 
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % clear




santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % ls
Dockerfile.django				docker-compose.override.debug.yml		manage.py
Dockerfile.integration-tests			docker-compose.override.dev.yml			nginx
Dockerfile.nginx				docker-compose.override.https.yml		readme-docs
LICENSE.md					docker-compose.override.integration_tests.yml	requirements.txt
README.md					docker-compose.override.unit_tests.yml		service-internal.yaml
SECURITY.md					docker-compose.override.unit_tests_cicd.yml	setup
_config.yml					docker-compose.yml				temp.json
app.json					docs						tests
components					dojo						wsgi.py
ct.yaml						helm						wsgi_params
docker						kubeless.json
santiagopaschoalick@FBSP-TECH-0365 django-DefectDojo % cd ..
santiagopaschoalick@FBSP-TECH-0365 Projetos % ls
AGENDA			EXPORT			MONGO-DUMP		OWASP			RUNDECK			django-DefectDojo
AUTOSCALE		GIT			MONGO-GUI		PERCONA			SAVEMONEY		kubeless
CLOUDFLARE		GRAFANA			MONGODB			POSTGRES		SECUREBOX		rundeck.yaml
CRON			HELLO-KUBERNETES	MONGODB-SANDBOX		POSTGRES-LOCALHOST	TOWER			tmp_velero
DEV			KAFKA			MSSQL			POSTGRES2		VELERO			virtmanager
DNS			KONG			MYSQL-OPERATOR		PROXYSQL		WORDPRESS
DOKUWIKI		KONG-LOCAL		NGINX-WEB		RANCHER			WORDPRESS2
DR			KONGA			NODERED			RANCHER-SINGLEINSTANCE	autoterraform
EASY			KUBERMETRICS		ODOO			REDIS			awx
ELASTICSEARCH		MEU			OPENSEARCH		REDIS-OPERATOR		devspace
santiagopaschoalick@FBSP-TECH-0365 Projetos % cd autoterraform 
santiagopaschoalick@FBSP-TECH-0365 autoterraform % ls
README.md	main.tf
santiagopaschoalick@FBSP-TECH-0365 autoterraform % nano main.tf 
santiagopaschoalick@FBSP-TECH-0365 autoterraform % 
santiagopaschoalick@FBSP-TECH-0365 autoterraform % 
santiagopaschoalick@FBSP-TECH-0365 autoterraform % cd ..   
santiagopaschoalick@FBSP-TECH-0365 Projetos % cd devspace  
cd: not a directory: devspace
santiagopaschoalick@FBSP-TECH-0365 Projetos % ls
AGENDA			EXPORT			MONGO-DUMP		OWASP			RUNDECK			django-DefectDojo
AUTOSCALE		GIT			MONGO-GUI		PERCONA			SAVEMONEY		kubeless
CLOUDFLARE		GRAFANA			MONGODB			POSTGRES		SECUREBOX		rundeck.yaml
CRON			HELLO-KUBERNETES	MONGODB-SANDBOX		POSTGRES-LOCALHOST	TOWER			tmp_velero
DEV			KAFKA			MSSQL			POSTGRES2		VELERO			virtmanager
DNS			KONG			MYSQL-OPERATOR		PROXYSQL		WORDPRESS
DOKUWIKI		KONG-LOCAL		NGINX-WEB		RANCHER			WORDPRESS2
DR			KONGA			NODERED			RANCHER-SINGLEINSTANCE	autoterraform
EASY			KUBERMETRICS		ODOO			REDIS			awx
ELASTICSEARCH		MEU			OPENSEARCH		REDIS-OPERATOR		devspace
santiagopaschoalick@FBSP-TECH-0365 Projetos % cd devspace 
cd: not a directory: devspace
santiagopaschoalick@FBSP-TECH-0365 Projetos % clear

santiagopaschoalick@FBSP-TECH-0365 Projetos % ls
AGENDA			EXPORT			MONGO-DUMP		OWASP			RUNDECK			django-DefectDojo
AUTOSCALE		GIT			MONGO-GUI		PERCONA			SAVEMONEY		kubeless
CLOUDFLARE		GRAFANA			MONGODB			POSTGRES		SECUREBOX		rundeck.yaml
CRON			HELLO-KUBERNETES	MONGODB-SANDBOX		POSTGRES-LOCALHOST	TOWER			tmp_velero
DEV			KAFKA			MSSQL			POSTGRES2		VELERO			virtmanager
DNS			KONG			MYSQL-OPERATOR		PROXYSQL		WORDPRESS
DOKUWIKI		KONG-LOCAL		NGINX-WEB		RANCHER			WORDPRESS2
DR			KONGA			NODERED			RANCHER-SINGLEINSTANCE	autoterraform
EASY			KUBERMETRICS		ODOO			REDIS			awx
ELASTICSEARCH		MEU			OPENSEARCH		REDIS-OPERATOR		devspace
santiagopaschoalick@FBSP-TECH-0365 Projetos % cd tmp_velero 
santiagopaschoalick@FBSP-TECH-0365 tmp_velero % ls
credentials-velero	velero-plugin-for-aws
santiagopaschoalick@FBSP-TECH-0365 tmp_velero % cd ..
santiagopaschoalick@FBSP-TECH-0365 Projetos % ls
AGENDA			EXPORT			MONGO-DUMP		OWASP			RUNDECK			django-DefectDojo
AUTOSCALE		GIT			MONGO-GUI		PERCONA			SAVEMONEY		kubeless
CLOUDFLARE		GRAFANA			MONGODB			POSTGRES		SECUREBOX		rundeck.yaml
CRON			HELLO-KUBERNETES	MONGODB-SANDBOX		POSTGRES-LOCALHOST	TOWER			tmp_velero
DEV			KAFKA			MSSQL			POSTGRES2		VELERO			virtmanager
DNS			KONG			MYSQL-OPERATOR		PROXYSQL		WORDPRESS
DOKUWIKI		KONG-LOCAL		NGINX-WEB		RANCHER			WORDPRESS2
DR			KONGA			NODERED			RANCHER-SINGLEINSTANCE	autoterraform
EASY			KUBERMETRICS		ODOO			REDIS			awx
ELASTICSEARCH		MEU			OPENSEARCH		REDIS-OPERATOR		devspace
santiagopaschoalick@FBSP-TECH-0365 Projetos % 
santiagopaschoalick@FBSP-TECH-0365 Projetos % 
santiagopaschoalick@FBSP-TECH-0365 Projetos % cd ..
santiagopaschoalick@FBSP-TECH-0365 ~ % ls
1.txt			Downloads		Postman			docker			mx.txt			sebastiao
2.txt			Library			Projetos		este.yaml		mysql.yaml		teste.save
Applications		Movies			Public			fretebank.com.br	nano.save		teste.sh
Chaves			Music			[0-9].*[0-9]		fretebras-com-br.txt	nano.save.1
Desktop			PROMETHEUS		ars.			getting-started		role
Documents		Pictures		chave.pem		lucas			salvi
santiagopaschoalick@FBSP-TECH-0365 ~ % find / -name terraform
find: /usr/sbin/authserver: Permission denied
find: /Library/Application Support/Apple/ParentalControls/Users: Permission denied
find: /Library/Application Support/Apple/AssetCache/Data: Permission denied
find: /Library/Application Support/Apple/Remote Desktop/Task Server: Permission denied
find: /Library/Application Support/Apple/Remote Desktop/Client: Permission denied
find: /Library/Application Support/ApplePushService: Permission denied
find: /Library/Application Support/TrendMicro/common/lib/RCM: Permission denied
find: /Library/Application Support/TrendMicro/common/lib/DCE: Permission denied
find: /Library/Application Support/TrendMicro/common/lib/CRC: Permission denied
find: /Library/Application Support/TrendMicro/common/lib/vsapi/quarantine: Permission denied
find: /Library/Application Support/TrendMicro/common/lib/vsapi/cleansave: Permission denied
find: /Library/Application Support/TrendMicro/common/lib/vsapi/cache: Permission denied
find: /Library/Application Support/TrendMicro/common/lib/vsapi/tmp: Permission denied
find: /Library/Application Support/TrendMicro/common/lib/icorex_cache: Permission denied
find: /Library/Application Support/TrendMicro/common/lib/TMFBE: Permission denied
find: /Library/Application Support/TrendMicro/common/lib/TMCSE: Permission denied
find: /Library/Application Support/TrendMicro/common/lib/AUlib: Permission denied
find: /Library/Application Support/TrendMicro/common/lib/unpack: Permission denied
find: /Library/Application Support/TrendMicro/common/lib/tmp: Permission denied
find: /Library/Application Support/TrendMicro/common/lib/TMUFE: Permission denied
find: /Library/Application Support/TrendMicro/TmccUpdate: Permission denied
find: /Library/Application Support/TrendMicro/aot: Permission denied
find: /Library/Application Support/com.trendmicro.iCoreSecurity/common/lib/vsapi: Permission denied
find: /Library/Application Support/com.trendmicro.iCoreSecurity/common/conf: Permission denied
find: /Library/Application Support/com.apple.TCC: Operation not permitted
find: /Library/Application Support/com.trendmicro.endpointbasecamp/common/conf: Permission denied
find: /Library/Application Support/ZeroTier/One/controller.d: Permission denied
find: /Library/Caches/Desktop Pictures/C3F55855-B124-473F-96F3-AD32E8DD14EE: Permission denied
find: /Library/Caches/com.apple.iconservices.store: Permission denied
find: /Library/Caches/com.apple.aned: Operation not permitted
find: /System/Library/DirectoryServices/DefaultLocalDB/Default: Permission denied
find: /System/Library/Templates/Data/Library/Application Support/Apple/ParentalControls/Users: Permission denied
find: /System/Library/Templates/Data/Library/Application Support/com.apple.TCC: Operation not permitted
find: /System/Library/Templates/Data/private/etc/cups/certs: Permission denied
find: /System/Library/Templates/Data/private/var/install: Permission denied
find: /System/Library/Templates/Data/private/var/ma: Permission denied
find: /System/Library/Templates/Data/private/var/spool/mqueue: Permission denied
find: /System/Library/Templates/Data/private/var/spool/postfix/saved: Permission denied
find: /System/Library/Templates/Data/private/var/spool/postfix/trace: Permission denied
find: /System/Library/Templates/Data/private/var/spool/postfix/defer: Permission denied
find: /System/Library/Templates/Data/private/var/spool/postfix/flush: Permission denied
find: /System/Library/Templates/Data/private/var/spool/postfix/deferred: Permission denied
find: /System/Library/Templates/Data/private/var/spool/postfix/corrupt: Permission denied
find: /System/Library/Templates/Data/private/var/spool/postfix/public: Permission denied
find: /System/Library/Templates/Data/private/var/spool/postfix/private: Permission denied
find: /System/Library/Templates/Data/private/var/spool/postfix/incoming: Permission denied
find: /System/Library/Templates/Data/private/var/spool/postfix/active: Permission denied
find: /System/Library/Templates/Data/private/var/spool/postfix/maildrop: Permission denied
find: /System/Library/Templates/Data/private/var/spool/postfix/hold: Permission denied
find: /System/Library/Templates/Data/private/var/spool/postfix/bounce: Permission denied
find: /System/Library/Templates/Data/private/var/spool/cups: Permission denied
find: /System/Library/Templates/Data/private/var/jabberd: Permission denied
find: /System/Library/Templates/Data/private/var/audit: Permission denied
find: /System/Library/Templates/Data/private/var/root: Permission denied
find: /System/Library/Templates/Data/private/var/lib/postfix: Permission denied
find: /System/Library/Templates/Data/private/var/db/appinstalld: Permission denied
find: /System/Library/Templates/Data/private/var/db/diskimagesiod: Permission denied
find: /System/Library/Templates/Data/private/var/db/locationd: Permission denied
find: /System/Library/Templates/Data/private/var/db/sysdiagnose/com.apple.sysdiagnose: Permission denied
find: /System/Library/Templates/Data/private/var/db/analyticsd: Permission denied
find: /System/Library/Templates/Data/private/var/db/rmd: Permission denied
find: /System/Library/Templates/Data/private/var/db/knowledgegraphd: Permission denied
find: /System/Library/Templates/Data/private/var/db/nsurlsessiond: Permission denied
find: /System/Library/Templates/Data/private/var/db/fpsd: Permission denied
find: /System/Library/Templates/Data/private/var/db/hidd: Permission denied
find: /System/Library/Templates/Data/private/var/db/installcoordinationd: Permission denied
find: /System/Library/Templates/Data/private/var/db/geod: Permission denied
find: /System/Library/Templates/Data/private/var/db/oah: Operation not permitted
find: /System/Library/Templates/Data/private/var/db/reportmemoryexception: Permission denied
find: /System/Library/Templates/Data/private/var/db/lockdown: Permission denied
find: /System/Library/Templates/Data/private/var/db/datadetectors: Permission denied
find: /System/Library/Templates/Data/private/var/db/cmiodalassistants: Permission denied
find: /System/Library/Templates/Data/private/var/db/com.apple.xpc.roleaccountd.staging: Permission denied
find: /System/Library/Templates/Data/private/var/db/dslocal/nodes/Default: Permission denied
find: /System/Library/Templates/Data/private/var/db/nearbyd: Permission denied
find: /System/Library/Templates/Data/private/var/db/timed: Permission denied
find: /System/Library/Templates/Data/private/var/db/applepay: Permission denied
find: /System/Library/Templates/Data/private/var/db/darwindaemon: Permission denied
find: /System/Library/Templates/Data/private/var/db/securityagent: Permission denied
find: /System/Library/Templates/Data/private/var/db/accessoryupdater: Permission denied
find: /System/Library/Templates/Data/private/var/db/ConfigurationProfiles/Store: Permission denied
find: /System/Library/Templates/Data/private/var/db/caches/opendirectory: Permission denied
find: /System/Library/Templates/Data/private/var/at/tabs: Permission denied
find: /System/Library/Templates/Data/private/var/at/tmp: Permission denied
find: /System/Library/Templates/Data/private/var/backups: Permission denied
find: /System/Library/Templates/Data/private/var/agentx: Permission denied
find: /System/Library/Caches/com.apple.coresymbolicationd: Permission denied
find: /System/Volumes/Update/Hardware: Permission denied
find: /System/Volumes/Update/Controller: Permission denied
find: /System/Volumes/Preboot/.Trashes: Operation not permitted
find: /System/Volumes/Data/.Spotlight-V100: No such file or directory
find: /System/Volumes/Data/boot: No such file or directory
find: /System/Volumes/Data/Library/Application Support/Apple/ParentalControls/Users: Permission denied
find: /System/Volumes/Data/Library/Application Support/Apple/AssetCache/Data: Permission denied
find: /System/Volumes/Data/Library/Application Support/Apple/Remote Desktop/Task Server: Permission denied
find: /System/Volumes/Data/Library/Application Support/Apple/Remote Desktop/Client: Permission denied
find: /System/Volumes/Data/Library/Application Support/ApplePushService: Permission denied
find: /System/Volumes/Data/Library/Application Support/TrendMicro/common/lib/RCM: Permission denied
find: /System/Volumes/Data/Library/Application Support/TrendMicro/common/lib/DCE: Permission denied
find: /System/Volumes/Data/Library/Application Support/TrendMicro/common/lib/CRC: Permission denied
find: /System/Volumes/Data/Library/Application Support/TrendMicro/common/lib/vsapi/quarantine: Permission denied
find: /System/Volumes/Data/Library/Application Support/TrendMicro/common/lib/vsapi/cleansave: Permission denied
find: /System/Volumes/Data/Library/Application Support/TrendMicro/common/lib/vsapi/cache: Permission denied
find: /System/Volumes/Data/Library/Application Support/TrendMicro/common/lib/vsapi/tmp: Permission denied
find: /System/Volumes/Data/Library/Application Support/TrendMicro/common/lib/icorex_cache: Permission denied
find: /System/Volumes/Data/Library/Application Support/TrendMicro/common/lib/TMFBE: Permission denied
find: /System/Volumes/Data/Library/Application Support/TrendMicro/common/lib/TMCSE: Permission denied
find: /System/Volumes/Data/Library/Application Support/TrendMicro/common/lib/AUlib: Permission denied
find: /System/Volumes/Data/Library/Application Support/TrendMicro/common/lib/unpack: Permission denied
find: /System/Volumes/Data/Library/Application Support/TrendMicro/common/lib/tmp: Permission denied
find: /System/Volumes/Data/Library/Application Support/TrendMicro/common/lib/TMUFE: Permission denied
find: /System/Volumes/Data/Library/Application Support/TrendMicro/TmccUpdate: Permission denied
find: /System/Volumes/Data/Library/Application Support/TrendMicro/aot: Permission denied
find: /System/Volumes/Data/Library/Application Support/com.trendmicro.iCoreSecurity/common/lib/vsapi: Permission denied
find: /System/Volumes/Data/Library/Application Support/com.trendmicro.iCoreSecurity/common/conf: Permission denied
find: /System/Volumes/Data/Library/Application Support/com.apple.TCC: Operation not permitted
find: /System/Volumes/Data/Library/Application Support/com.trendmicro.endpointbasecamp/common/conf: Permission denied
find: /System/Volumes/Data/Library/Application Support/ZeroTier/One/controller.d: Permission denied
find: /System/Volumes/Data/Library/Caches/Desktop Pictures/C3F55855-B124-473F-96F3-AD32E8DD14EE: Permission denied
find: /System/Volumes/Data/Library/Caches/com.apple.iconservices.store: Permission denied
find: /System/Volumes/Data/Library/Caches/com.apple.aned: Operation not permitted
find: /System/Volumes/Data/System/Library/DirectoryServices/DefaultLocalDB/Default: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/Library/Application Support/Apple/ParentalControls/Users: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/Library/Application Support/com.apple.TCC: Operation not permitted
find: /System/Volumes/Data/System/Library/Templates/Data/private/etc/cups/certs: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/install: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/ma: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/spool/mqueue: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/spool/postfix/saved: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/spool/postfix/trace: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/spool/postfix/defer: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/spool/postfix/flush: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/spool/postfix/deferred: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/spool/postfix/corrupt: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/spool/postfix/public: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/spool/postfix/private: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/spool/postfix/incoming: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/spool/postfix/active: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/spool/postfix/maildrop: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/spool/postfix/hold: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/spool/postfix/bounce: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/spool/cups: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/jabberd: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/audit: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/root: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/lib/postfix: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/appinstalld: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/diskimagesiod: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/locationd: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/sysdiagnose/com.apple.sysdiagnose: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/analyticsd: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/rmd: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/knowledgegraphd: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/nsurlsessiond: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/fpsd: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/hidd: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/installcoordinationd: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/geod: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/oah: Operation not permitted
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/reportmemoryexception: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/lockdown: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/datadetectors: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/cmiodalassistants: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/com.apple.xpc.roleaccountd.staging: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/dslocal/nodes/Default: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/nearbyd: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/timed: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/applepay: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/darwindaemon: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/securityagent: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/accessoryupdater: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/ConfigurationProfiles/Store: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/db/caches/opendirectory: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/at/tabs: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/at/tmp: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/backups: Permission denied
find: /System/Volumes/Data/System/Library/Templates/Data/private/var/agentx: Permission denied
find: /System/Volumes/Data/System/Library/Caches/com.apple.coresymbolicationd: Permission denied
^C
santiagopaschoalick@FBSP-TECH-0365 ~ % 
santiagopaschoalick@FBSP-TECH-0365 ~ % 
santiagopaschoalick@FBSP-TECH-0365 ~ % 
santiagopaschoalick@FBSP-TECH-0365 ~ % cd Projetos 
santiagopaschoalick@FBSP-TECH-0365 Projetos % ls
AGENDA			EXPORT			MONGO-DUMP		OWASP			RUNDECK			django-DefectDojo
AUTOSCALE		GIT			MONGO-GUI		PERCONA			SAVEMONEY		kubeless
CLOUDFLARE		GRAFANA			MONGODB			POSTGRES		SECUREBOX		rundeck.yaml
CRON			HELLO-KUBERNETES	MONGODB-SANDBOX		POSTGRES-LOCALHOST	TOWER			tmp_velero
DEV			KAFKA			MSSQL			POSTGRES2		VELERO			virtmanager
DNS			KONG			MYSQL-OPERATOR		PROXYSQL		WORDPRESS
DOKUWIKI		KONG-LOCAL		NGINX-WEB		RANCHER			WORDPRESS2
DR			KONGA			NODERED			RANCHER-SINGLEINSTANCE	autoterraform
EASY			KUBERMETRICS		ODOO			REDIS			awx
ELASTICSEARCH		MEU			OPENSEARCH		REDIS-OPERATOR		devspace
santiagopaschoalick@FBSP-TECH-0365 Projetos % cd DR
santiagopaschoalick@FBSP-TECH-0365 DR % ls
terraformando-eks
santiagopaschoalick@FBSP-TECH-0365 DR % cd terraformando-eks 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % ls
README.md	kubernetes	modules		modules.tf	output.tf	provider.tf	variables.tf
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % nano README.md 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % nano modules
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % cd modules
santiagopaschoalick@FBSP-TECH-0365 modules % ls
network
santiagopaschoalick@FBSP-TECH-0365 modules % cd ..
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % ls
README.md	kubernetes	modules		modules.tf	output.tf	provider.tf	variables.tf
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % cd modules.tf 
cd: not a directory: modules.tf
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % cat modules.tf
module "network" {
  source = "./modules/network"
  
  cluster_name  = var.cluster_name
  aws_region    = var.aws_region
}

module "master" {
  source = "./modules/master"

  cluster_name  = var.cluster_name
  aws_region    = var.aws_region
  k8s_version   = var.k8s_version

  cluster_vpc   = module.network.cluster_vpc
  private_subnet_1a   = module.network.private_subnet_1a
  private_subnet_1c   = module.network.private_subnet_1c
}

module "nodes" {
  source = "./modules/nodes"

  cluster_name        = var.cluster_name
  aws_region          =  var.aws_region
  k8s_version         = var.k8s_version

  cluster_vpc         = module.network.cluster_vpc
  private_subnet_1a   = module.network.private_subnet_1a
  private_subnet_1c   = module.network.private_subnet_1c

  eks_cluster         = module.master.eks_cluster
  eks_cluster_sg      = module.master.security_group

  nodes_instances_sizes   = var.nodes_instances_sizes
  auto_scale_options      = var.auto_scale_options

  auto_scale_cpu     = var.auto_scale_cpu
}
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % ls            
README.md	kubernetes	modules		modules.tf	output.tf	provider.tf	variables.tf
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % pwd
/Users/santiagopaschoalick/Projetos/DR/terraformando-eks
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % nano output.tf 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % nano provider.tf 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % nano variables.tf 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % nano modules.tf 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % ls
README.md	kubernetes	modules		modules.tf	output.tf	provider.tf	variables.tf
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % cd modules
santiagopaschoalick@FBSP-TECH-0365 modules % ls
network
santiagopaschoalick@FBSP-TECH-0365 modules % cd network 
santiagopaschoalick@FBSP-TECH-0365 network % ls
internet.tf	nat-gateway.tf	output.tf	private.tf	public.tf	variables.tf	vpc.tf
santiagopaschoalick@FBSP-TECH-0365 network % nano internet.tf 
santiagopaschoalick@FBSP-TECH-0365 network % nano output.tf  
santiagopaschoalick@FBSP-TECH-0365 network % nano public.tf 
santiagopaschoalick@FBSP-TECH-0365 network % nano variables.tf 
santiagopaschoalick@FBSP-TECH-0365 network % nano vpc.tf 
santiagopaschoalick@FBSP-TECH-0365 network % 
santiagopaschoalick@FBSP-TECH-0365 network % 
santiagopaschoalick@FBSP-TECH-0365 network % 
santiagopaschoalick@FBSP-TECH-0365 network % 
santiagopaschoalick@FBSP-TECH-0365 network % 
santiagopaschoalick@FBSP-TECH-0365 network % ls
internet.tf	nat-gateway.tf	output.tf	private.tf	public.tf	variables.tf	vpc.tf
santiagopaschoalick@FBSP-TECH-0365 network % nano internet.tf 
santiagopaschoalick@FBSP-TECH-0365 network % 
santiagopaschoalick@FBSP-TECH-0365 network % 
santiagopaschoalick@FBSP-TECH-0365 network % nano variables.tf 
santiagopaschoalick@FBSP-TECH-0365 network % nano vpc.tf 
santiagopaschoalick@FBSP-TECH-0365 network % 
santiagopaschoalick@FBSP-TECH-0365 network % 
santiagopaschoalick@FBSP-TECH-0365 network % 
santiagopaschoalick@FBSP-TECH-0365 network % ls
internet.tf	nat-gateway.tf	output.tf	private.tf	public.tf	variables.tf	vpc.tf
santiagopaschoalick@FBSP-TECH-0365 network % nano internet.tf 
santiagopaschoalick@FBSP-TECH-0365 network % 
santiagopaschoalick@FBSP-TECH-0365 network % 
santiagopaschoalick@FBSP-TECH-0365 network % 
santiagopaschoalick@FBSP-TECH-0365 network % cd ..
santiagopaschoalick@FBSP-TECH-0365 modules % ls
network
santiagopaschoalick@FBSP-TECH-0365 modules % cd ..
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % ls
README.md	kubernetes	modules		modules.tf	output.tf	provider.tf	variables.tf
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % nano variables.tf 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % nano README.md 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % nano README.md
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % LS
README.md	kubernetes	modules		modules.tf	output.tf	provider.tf	variables.tf
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % CAT README.md 
<h1 align="center">FRETEBRAS-DR 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-v0-blue.svg?cacheSeconds=2592000" />
  <a href=".docs/" target="_blank">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" />
  </a>
  <a href="LICENSE" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-yellow.svg" />
  </a>
  <a href="https://twitter.com/fidelissauro" target="_blank">
    <img alt="Twitter: fidelissauro" src="https://img.shields.io/twitter/follow/fidelissauro.svg?style=social" />
  </a>
</p>

> Codebase da série de videos Terraformando o EKS no Youtube

### 🏠 [Guia](/)

* **Aula #00 - Conceitos básicos e VPC** - [Exemplos](https://github.com/msfidelis/terraformando-eks/tree/aula00_vpc) - [Video](https://www.youtube.com/watch?v=-ghbb9PyGxY)

* **Aula #01 - Terraformando o EKS Cluster** - [Exemplos](https://github.com/msfidelis/terraformando-eks/tree/aula01_eks) - [Video](https://www.youtube.com/watch?v=-ghbb9PyGxY)

* **Aula #02 - Node groups** - [Exemplos](https://github.com/msfidelis/terraformando-eks/tree/aula02_nodes) - [Video](https://www.youtube.com/watch?v=kXqiqZ5Nap8)

* **Aula #03 - Traefik no EKS** - [Exemplos](https://github.com/msfidelis/terraformando-eks/tree/aula03_traefik) - [Video](https://www.youtube.com/watch?v=ThONqZT2Mfs&t=9s)

* **Aula #04 - Auto Scale do Cluster** - [Exemplos](https://github.com/msfidelis/terraformando-eks/tree/aula04_scale) - [Video](https://www.youtube.com/watch?v=tYikrqYRAaQ)

### ✨ [Demo](/)

## Instalação

```sh
terraform init
```

## Aplicando

```sh
terraform apply --auto-approve
```

## Validação

```sh
terraform validate
```

## Adicionando o contexto do nosso cluster ao kubectl

```bash
aws eks --region us-east-1 update-kubeconfig --name nome-do-cluster
aws eks --region us-east-1 update-kubeconfig --name k8s-demo
```

```bash
kubectl get nodes
```

## Deploy o Ingress

```bash
kubectl apply -f kubernetes/traefik/ingress.yml
```

## Deploy demo services

* [Whois App](https://github.com/msfidelis/microservice-nadave-whois)
* [Faker App](https://github.com/msfidelis/microservice-nadave-fake-person)
* [Pudim](https://github.com/msfidelis/pudim)

```bash
kubectl apply -f kubernetes/apps/whois.yml
kubectl apply -f kubernetes/apps/faker.yml
kubectl apply -f kubernetes/apps/pudim.yml
```

## Deploy do Metric Server

```bash
kubectl apply -f kubernetes/metric-server/metric-server.yml
```

## Author

👤 **Matheus Fidelis**

* Website: https://raj.ninja
* Twitter: [@fidelissauro](https://twitter.com/fidelissauro)
* Github: [@msfidelis](https://github.com/msfidelis)
* LinkedIn: [@msfidelis](https://linkedin.com/in/msfidelis)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](/issues). 

## Show your support

Give a ⭐️ if this project helped you!

## 📝 License

Copyright © 2020 [Matheus Fidelis](https://github.com/msfidelis).<br />
This project is [MIT](LICENSE) licensed.

***
_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % CLEAR

santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % LS
README.md	kubernetes	modules		modules.tf	output.tf	provider.tf	variables.tf
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % NANO README.md 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % CLEAR






























santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % A
zsh: command not found: A
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % A
zsh: command not found: A
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % A
zsh: command not found: A
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % A
zsh: command not found: A
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % A
zsh: command not found: A
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % A
zsh: command not found: A
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % CLEAR







santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % nano README.md 




































  GNU nano 2.0.6                                       File: README.md                                                                                      

kubectl apply -f kubernetes/metric-server/metric-server.yml
```

## Author

👤 **Matheus Fidelis**

* Website: https://raj.ninja
* Twitter: [@fidelissauro](https://twitter.com/fidelissauro)
* Github: [@msfidelis](https://github.com/msfidelis)
* LinkedIn: [@msfidelis](https://linkedin.com/in/msfidelis)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](/issues).

## Show your support

Give a  ️ if this project helped you!

## 📝 License

Copyright © 2020 [Matheus Fidelis](https://github.com/msfidelis).<br />
This project is [MIT](LICENSE) licensed.

***
_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
