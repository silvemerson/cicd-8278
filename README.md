# 524 - Integração e Entrega Continua com Git, Jenkins, Nexus e Sonar - LC

Repositório de apoio ao curso

```
Instrutor: Emerson Silva

In: https://www.linkedin.com/in/silvemerson/

Turma: 8278

Github: https://github.com/4linux/524/tree/k3s
```

## Gitea

```
cd gitea
docker-compose up -d
```

## Jenkins Install

```
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt-get update

sudo apt-get install openjdk-11-jdk -y

sudo apt-get install jenkins -y
```

### Jenkins Plugins

- Docker Pipeline
- SonarQube Scanner
- Nexus Platform
- Pipeline Utility Steps
- Gitea
- Gogs
- Locale
- Kubernetes

#### Configurando plugin Kubernetes

1. Copie o kube config

``` cp /etc/rancher/k3s/k3s.yaml ~/kubeconfig ```

2. Edit o arquivo do kubeconfig e adicione o IP da VM de k3s ```192.168.88.30```

3. Crie uma Credencial no Jenkins


