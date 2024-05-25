# projetinhobolado
Projeto para apresentar na entrevista da uol

* aws ec2 create-key-pair --key-name chavebolada --query 'KeyMaterial' --output text > chaveboladaprivada

* aws cloudformation create-stack --stack-name MeuStack --template-body file://cloudformation.yaml --parameters ParameterKey=KeyName,ParameterValue=chavebolada

* aws ec2 describe-instances | grep PublicIpAddress

* mudar os secrets