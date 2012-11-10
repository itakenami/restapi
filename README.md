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

	```play dependencies```
	
## Testando

Para criar um exmplo, dentro da pasta do projeto, utilize o comando:
	restapi:sample
	
Após executar o comando acima os seguintes arquivos serão criados:
* app/models/Usuario.java => Model exemplo
* app/controllers/Usuarios.java => Controlador com as abstrações contidas na LIB play-rest
* app/controllers/Wadl.java => Controller para gerar arquivo WADL do projeto
* conf/result_messages.properties => Mensagens de retorno

Além dos arquivos criados, uma configuração adicionar será incluida nos seguintes arquivos:
* conf/application.conf
* conf/routes

Para testar utilize as URLs:
* http://localhost:9000/api/wadl => Arquivo WADL
* http://localhost:9000/api/clientes => Método GET que obter uma lista de Clientes