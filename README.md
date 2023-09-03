# Desafio Docker Golang
Desafio proposto pelo Wesley para manipulação de dockers e desenvolvimento local  
dentro do container montai um docker com go lang pra fazer o exemplo de Go pra  
imprimir a mensagem e colcoquei o executavel em outro build de docker e procurei  
a melhor imagem para executar o binario gerado como fosse uma aplicação dem produção.

- [x] Executavel com golang com menos de 2mb (3.14mb no dockerhub)

__obs: Eu não sei se consegui atingir a meta do desafio porque não encontrei nenhuma  
distribuição que fosse menor de 1 mb pra poder criar uma imagem dockerhub menor__

## Repositorio das imagens docker no dockerhub pacalexandre
```resultado```
- https://hub.docker.com/r/pacalexandre/fullcycle

## Documentação GoLang.
- https://go.dev/doc/tutorial/getting-started

Programando em Golang  
build executvel para linux/386

```go build -o full```


## Versões instaladas em meu ambiente.
```bash 
NAME="Linux Mint"
VERSION="21.1 (Vera)"
ID=linuxmint
ID_LIKE="ubuntu debian"
PRETTY_NAME="Linux Mint 21.1"
VERSION_ID="21.1"
HOME_URL="https://www.linuxmint.com/"
SUPPORT_URL="https://forums.linuxmint.com/"
BUG_REPORT_URL="http://linuxmint-troubleshooting-guide.readthedocs.io/en/latest/"
PRIVACY_POLICY_URL="https://www.linuxmint.com/"
VERSION_CODENAME=vera
UBUNTU_CODENAME=jammy

Docker version 24.0.5, build ced0996
Docker Compose version v2.20.2
```
## Comando utilizados.

```bash
#No terminal para subior projeto parar editar em go 
docker compose up --build -d

docker build -t pacalexandre/fullcycle -f Dockerfile.desafio .

docker login

docker push pacalexandre/fullcycle

docker rm $(docker ps -a -q )

```