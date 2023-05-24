
# Montando a infraestrutura

Comece instando o [minikube](https://minikube.sigs.k8s.io/docs/start/) de acordo com a documentação.

Com ele instalado na sua máquina, execute o comando

```
minikube start
```

para iniciar o cluster do kubernetes localmente.

Para podermos interagir com o cluster instale o [kubectl](https://kubernetes.io/docs/tasks/tools/) de acordo com a documentação.

# Iniciando a aplicação

Para criar a aplicação dentro do cluster execute o comando

```
kubectl apply -f Voll-med.yaml
```

E para que o balanceador de carga funcione, abra outro terminal e execute

### linux
```
ip addr
```

### windows
```
ipconfig
```


anote o endereço de IP mostrado e em seguida inicie o tunel do minikube.

```
minikube tunnel --bind-address=
```

seguido do seu endereço de IP.




---

# Versão do NodeJS

- Nesse projeto estamos usando a versão **16.0.0** do NodeJS

# Iniciando o projeto

Depois de baixar o código para a sua máquina, execute o comando

```
npm install
```

Esse comando irá instalar todas as dependencias do projeto na sua máquina.

## Executando o projeto

Depois de instalar todas as dependências execute o comando

```
npm start
```

Assim o seu projeto será compilado e o servidor será esecutado na url `localhost:3000`


