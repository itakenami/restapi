Adicione esta configuração em dependencies.yml para instalar o módulo

    # Application dependencies
    require:
        - play
        - takenami -> restapi 0.

    # My custom repositories
    repositories:
        - takenami:
            type:       http
            artifact:   "http://cloud.github.com/downloads/itakenami/restapi/[module]-[revision].zip"
            contains:
                - takenami -> *