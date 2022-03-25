Esse blog me ajudou muito na compreensão, fiz esse fork apenas para ajustar com o meu ambiente de estudos, atualizando a versão do fluentbit e configurando para uso do fluent bit com o conteinerd. Seguindo a doc de instalação no kubernetes. [Acesso a doc](https://docs.fluentbit.io/manual/installation/kubernetes#installation) em 24/03/2022.

# Fluent Bit Configuration for K8s and Graylog

> See [this blog post](https://vzurczak.wordpress.com/?p=781) for more details.

A K8s configuration to install and configure Fluent Bit as a daemon set.  
Fluent Bit collects only Docker logs, gets K8s metadata, builds a GEF message
and sends it to a Graylog server.

* Update the **fluent-bit-configmap.yaml** file.
  Replace **192.168.1.18** with the IP address of your Graylog server.
* Then execute the **deploy.sh** script.

