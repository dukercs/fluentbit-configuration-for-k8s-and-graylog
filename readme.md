Esse blog me ajudou muito na compreensão, fiz esse fork apenas para ajustar com o meu ambiente de estudos, atualizando a versão do fluentbit e configurando para uso do fluent bit com o conteinerd. Seguindo a doc de instalação no kubernetes. [Acesso a doc](https://docs.fluentbit.io/manual/installation/kubernetes#installation) em 24/03/2022.

Meu ambiente de treinamento seguindo o livro [Descomplicando o Kubernetes](https://livro.descomplicandokubernetes.com.br/pt/day_one/descomplicando_kubernetes.html#instala%C3%A7%C3%A3o-em-cluster-com-tr%C3%AAs-n%C3%B3s) acessado em 25/03/2022, do fabuloco [Jeferson](https://twitter.com/badtux_) 

Instalação do Graylog seguindo a [documentação](https://docs.graylog.org/v1/docs/ubuntu) acessada em 25/03/2022.

No arquivo de [ConfigMap](https://github.com/dukercs/fluentbit-configuration-for-k8s-and-graylog/blob/master/fluent-bit-configmap.yaml) ajuste próximo as linhas 64 e 65 o IP e porta do Graylog, o resto é muito simples rode o deploy.sh que vai usar o kubectl para criar os yaml no seu cluster k8s.

# Fluent Bit Configuration for K8s and Graylog

> See [this blog post](https://vzurczak.wordpress.com/?p=781) for more details.

A K8s configuration to install and configure Fluent Bit as a daemon set.  
Fluent Bit collects only Docker logs, gets K8s metadata, builds a GEF message
and sends it to a Graylog server.

* Update the **fluent-bit-configmap.yaml** file.
  Replace **192.168.1.18** with the IP address of your Graylog server.
* Then execute the **deploy.sh** script.

