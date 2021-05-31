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

ESLINT
Instalar o plugins do vscode eslint
npx eslint --init

2 opção checar a syntax e encontrar o problemas,na frente iremos deixar no prettier para regras

ah 3 opção seria as regras, mas no momento não iremos fazer

javascript modules( import/export)
React
Yes
Browser
JSON


usando yarn
responder No

e depois
yarn add --dev eslint-plugin-react@latest @typescript-eslint/eslint-plugin@latest @typescript-eslint/parser@latest eslint@latest



PLUGINS PRA VER SE ESTÁ SENDO USADO DE FORMA CORRETA OS HOOKS
https://www.npmjs.com/package/eslint-plugin-react-hooks

yarn add eslint-plugin-react-hooks --dev

Iremos add abaixo:

{
  "plugins": [
    // ...
    "react-hooks"
  ],
  "rules": {
    // ...
    "react-hooks/rules-of-hooks": "error",
    "react-hooks/exhaustive-deps": "warn"
  }
}
depois iremos desligar o prop-types, pq estamos usando o type script

"react/prop-types": "off"
outra regra que precisamos desligar do react
"react/react-in-jsx-scope":"off"
outra regra que precisamos desligar do typescript
essa regra é sobre a tipagem quando o typescript identificar o tipo não precisa tipar

"@typescript-eslint/explicit-module-boundary-types":"off"

Por fim teremos mais uma configuração quando o eslint rodar ele precisa saber a versão do react e colocamos na config abaixo:

"settings":{
  "react":{
    "version": "detect"
  }
}


Para fazer um teste na pasta se tem algum erro de eslint podemos rodar


eslint src no terminal ou

cadastrar no package.json no scrits
"lint": "eslint src"

e rodar no terminal

yarn lint


===

PRETTIER
yarn add --dev --exact prettier

Criaremos um arquivo .prettierrc

colocaremos tb algumas configurações dentro

{
  "tralingComma":"none",
  "semi": false,
  "singleQuote": true
}

Precisamos instalar dois plugins

yarn add --dev eslint-plugin-prettier eslint-config-prettier

após isso iremos incluir no eslint

dentro de  extends
 "plugin:prettier/recommended"

 Depois criaremos uma pasta
 .vscode dentro da pasta
 settings.json

 e dentro colocaremos as configurações dentro


dentro de eslintrc.json

no rules:{
    "prettier/prettier": ["error",{
        "endOfLine": "auto"}
      ]
}

dentro do settings.json
{
"files.eol": "\n",
}


===









