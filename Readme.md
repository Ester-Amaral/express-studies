 # Este repositório reúne materiais de autoestudo de express e node.js

 ## Configuração do projeto
 ### Inicializão do node
 Quando criar um novo projeto é necessário inicializar o node, o que gera um arquivo chamado "package.json":  
        npm init -y
 ### Configuração do Typescript
Agora é preciso configurar o node para rodar typescript:  
        npm -D typescript, @types/node  
Inicializar e configurar o package de typescript,irá gerar o arquivo "tsconfig.json":
        npx -init
        tsc -init  
Deixar o arquivo "tsconfig.json" da seguinte maneira:
        {
            "compilerOptions": {
                
                /* Language and Environment */
                "target": "ESNext",    /* Set the JavaScript language version for emitted JavaScript and include compatible library declarations. */
                "lib": [],                    /* Specify a set of bundled library declaration files that describe the target runtime environment. */
                

                /* Modules */
                "module": "commonjs",                                /* Specify what module code is generated. */
                "rootDir": "./",                                  /* Specify the root folder within your source files. */
                "resolveJsonModule": true,                        /* Enable importing .json files. */
                

                /* Emit */
                "outDir": "./build",                                   /* Specify an output folder for all emitted files. */

                /* Interop Constraints */
                "esModuleInterop": true,  /* Emit additional JavaScript to ease support for importing CommonJS modules. This enables 'allowSyntheticDefaultImports' for type compatibility. */
                
                "forceConsistentCasingInFileNames": true,            /* Ensure that casing is correct in imports. */

                /* Type Checking */
                "strict": true,                                      /* Enable all strict type-checking options. */

                /* Completeness */
                "skipLibCheck": true                                 /* Skip type checking all .d.ts files. */
            },
            "include": [
                "src","package.json"
            ]
        }
Para finalizar a configuração do typescript, no arquivo "package.json", na sessão script adiciona a diretiva abaixo:
        "build":"tsc"
Teste as configurações com:
        npm run build
### Configuração do express
Instale o package express:
        npm install express
Agora instale as dependencias express:
        npm -D nodemon
## Atenção!!!
Caso o projeto já esteja configurado ou seja clone do github basta utilizar o comando:
        npm install
Ele instala-rá todos os packages e dependencias do projeto.