# Desafio Fullcycle Docker

Desafio proposto pelo Wesley para manipulação de dockers e desenvolvimento local 
- [ ] Imagem com golang com menos de 2mb (3.14)
- [x] Nodejs como express gravando em um banco de dados e dando display 

__obs: Eu não consegui atingir a meta do desafio porque não encontrei nenhuma  
distribuição que fosse menor de 1 mb pra poder criar uma imagem dockerhub__

## Repositorio das imagens docker no dockerhub
- https://hub.docker.com/r/pacalexandre/fullcycle

## Documentação GoLang
- https://go.dev/doc/tutorial/getting-started

Programando em Golang  
build executvel para linux/386

```go build -o full```


## Versões isntaladas em meu ambiente 
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
## Comando utilizados 

```bash
#No terminal para subior projeto parar editar em go 
docker compose up --build -d

docker build -t pacalexandre/fullcycle -f Dockerfile.desafio .

docker login

docker push pacalexandre/fullcycle

docker rm $(docker ps -a -q )

```