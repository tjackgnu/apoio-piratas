# apoio-piratas

`PEQUENO PROJETO DE APOIO AO PARTIDO PIRATA`

Instruções sobre como instalar as dependências e rodar o site.

O site depende de Django, instale usando pip (pip3 pois preferimos Python 3).
```
$ sudo pip3 install django
```

Se precisar instale o pip primeiro, use o instalador de pacotes da distribuição linux de sua escolha.

Tire um git clone do repositório:
```
$ git clone https://github.com/piratas/apoio-piratas.git
```

Para rodar em modo desenvolvedor, chame de dentro do diretório `apoio/` o seguinte comando:
```
$ python3 manage.py runserver
```

=======

# Rodando com Docker ou Docker-compose

Para instalar o docker siga:

Mac: https://docs.docker.com/mac/
Linux: https://docs.docker.com/linux/
Windows: https://docs.docker.com/windows/


## Docker only

```
$ docker build -t piratas/apoio .
$ docker run -d -p 8000:8000 piratas/apoio
```

Montando o diretorio para desenvolvimento:

```
$ docker run -d -p 8000:8000 -v $PWD/apoio:/app/apoio piratas/apoio
```

## Docker compose

```
$ docker-compose up -d
```

Acesse via:

Linux:http://127.0.0.1:8000

Mac ou Windows: http://192.168.99.100:8000 (caso não funcione, pegue o IP da docker-machine com:  $docker-machine ip
