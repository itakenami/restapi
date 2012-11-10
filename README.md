# RESTAPI

Modulo para Play 1.2.x que utiliza a biblioteca play-rest para implementar serviços REST de forma simples e organizada.

## Como instalar

Instale o Play 1.2.x e crie um novo projeto como descrito no link: http://www.playframework.org/documentation/1.2.5/install

Adicione esta configuração em conf/dependencies.yml

    # Application dependencies
    require:
        - play
        - takenami -> restapi 0.1

    # My custom repositories
    repositories:
        - takenami:
            type:       http
            artifact:   "http://cloud.github.com/downloads/itakenami/restapi/[module]-[revision].zip"
            contains:
                - takenami -> *

Dentro da pasta do projeto rode o comando:
   play dependencies

