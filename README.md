# Criação da imagem

Após configurar o arquivo Dockerfile, foi executado o seguinte comando para criar a imagem:

docker build -t ubuntu-nginx:1.0 .

Ao final, foi concluido com a criação da imagem ubuntu-nginx:1.0


# README.md

Para atender a solicitação do trabalho aplicado, foi criado um Dockerfile, criando a imagem ubuntu-nginx, uma imagem do ubuntu 18, com o nginx empacotado.

Ubuntu é um sistema operacional ou sistema operativo de código aberto, construído a partir do núcleo Linux, baseado no Debian e utiliza GNOME como ambiente de desktop de sua mais recente versão com suporte de longo prazo. É desenvolvido pela Canonical Ltd

Nginx é um servidor leve de HTTP, proxy reverso, proxy de e-mail IMAP/POP3, feito por Igor Sysoev em 2005, sob licença BSD-like 2-clause. O Nginx consome menos memória que o Apache, pois lida com requisições Web do tipo “event-based web server”; e o Apache é baseado no “process-based server”, podendo trabalhar juntos.
Ele é um servidor da web com uma arquitetura orientada a eventos, não encadeada, que permite que o Apache seja configurado corretamente, também pode fazer coisas importantes, como balanceamento de carga e acesso ao cache HTTP.

# Geracao do container

Para gerar o container é necessario fazer download da imagem no link abaixo:

https://hub.docker.com/repository/docker/juliocos/ubuntu-nginx

Após baixar a imagem e ter o docker instalado no computador, pelo terminal acessar a pasta onde a imagem foi salva e digitar o seguinte comando:

docker images

Sera exibido as imagens presentes
Para testar a imagem, basta criar um container, com o comando:

docker container run --name teste -p 80:80 ubuntu-nginx:1.0

Agora abra um navegador web e acesse http://localhost e será exibida a página padrão do nginx
Caso deseje pode subir um cotainer com o nome nginx, para facilitar a identificaçao do mesmo, com o comando: 

docker container run --name nginx -p 80:80 ubuntu-nginx:1.0
