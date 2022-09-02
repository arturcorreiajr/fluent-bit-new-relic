
## Criando imagem e subindo serviço
```console
docker build -t arturcorreiajunior/fluent-bit:latest .
```
```console
docker push arturcorreiajunior/fluent-bit:latest
```
Subindo a imagem no docker
```console
docker run -p 8080:5170 arturcorreiajunior/fluent-bit:latest 
```
Subindo a imagem no kubernetes
```console
kubectl apply -f yaml/fluent-bit-deploy.yaml
```
Enviando mensagem via terminal
```console
echo '{"message": "Mensagem"}' | nc 127.0.0.1 8080
```