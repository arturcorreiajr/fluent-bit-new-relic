
docker build -t arturcorreiajunior/fluent-bit-new-relic:latest .
docker push arturcorreiajunior/fluent-bit-new-relic:latest
docker run -p 8080:5170 arturcorreiajunior/fluent-bit-new-relic:latest 

kubectl apply -f yaml/fluent-bit-deploy.yaml

echo '{"key 1": "teste log", "key 2": "teste"}' | nc 127.0.0.1 52313