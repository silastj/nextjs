ANOTAÇÕES - SILAS

yarn create next-app
name ( boilerplate )
Precisa ter antes o node 10.13.0

===
yarn dev
    Starts the development server.

  yarn build
    Builds the app for production.

  yarn start
    Runs the built app in production mode.

===

DELETANDO A PASTA API
Next faz rota bem bacana , mas não precisamos no momento


DELETANDO _APP.JS
O arquivo muito importante, mas iremos deletar
Encapsular todos os components a nivel de página
Depois  criaremos ele novamente.

DELETAR O CSS GLOBALS

===
IREMOS LEVANTAR O PROJETO
yarn dev

===
CONFIGURANDO O TYPESCRIPT NO NEXTJS
Digite isso no terminal ou cria o arquivo manualmente
touch tsconfig.json

após dando yarn dev, ele precisa de algumas instalações abaixo:
obs( --dev apenas em desenvolvimento)

yarn add --dev typescript @types/react

Iremos alterar o tsconfig.json
 "strict": false, para  "strict": true,

 Esse arquivo ele analisa se a tipagem do typescript está restrito deixando no true, quando se pega projeto em andamento mesclando com javascript , deixamos com o valor em false

 Criaremos uma pasta src e colocamos a pasta pages dentro
 o arquivo index.js mudaremos para index.tsx

 .ts apenas typescript
 .tsx html dentro do typescript

===

 CONFIGURANDO O EDITORCONFIG
 Criaremos o arquivo .editorconfig

 com as configurações abaixo:
 #editorconfig.org

root = true


[*]
indent_style = space
indent_size = 2
end_of_line = lf
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true

===







