
# RESTAPI

Modulo para Play 1.2.x que utiliza a biblioteca play-rest para implementar serviços REST de forma simples e organizada.

## Como instalar

Adicione esta configuração em dependencies.yml para instalar o módulo

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