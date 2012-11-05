# Application dependencies

require:
    - play
    - restapi -> restapi 0.1

# My custom repositories
repositories:
    - zenexity:
        type:       http
        artifact:   "https://github.com/itakenami/restapi/blob/master/dist/[module]-[revision].zip?raw=true"
        contains:
            - restapi -> *