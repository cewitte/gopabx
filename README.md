# gopabx
Um gerador de textos para URAs feito em Go (Golang), que utiliza as APIs de text-to-speech to Google Cloud.

## Importante
Para usar esse app, você precisará configurar sua conta no Google Cloud, projeto, credenciais, etc. Eu não poderia explicar melhor do que faz o Google [aqui](https://cloud.google.com/text-to-speech/docs/quickstart-client-libraries?hl=pt-br).

A propósito, meu código usa como base o código disponível no Guia de início rápido do artigo linkado acima, com algumas diferenças:

1. Eu setei a única voz (feminina, baseada em Wavenet) disponível em português do Brasil.
1. Ao invés de utilizar uma `string` dentro do próprio código, meu código espera receber um arquivo `ssml` como argumento na linha de comando, por exemplo:

    `go run main.go -ssml=arquivo.ssml`

Se o nome é `arquivo.ssml`, ao terminar o app terá gerado um mp3 de nome `arquivo.mp3` no diretório raiz da aplicação.

## Sobre o SSML

A linguagem de marcação de síntese de fala (SSML, na sigla em inglês) tem sintaxe similar ao XML e permite controle maior sobre o resultado da voz sintetizada com pausas, formatação de áudio para acrônimos, datas, horas e abreviaturas ou texto a ser censurado.

Você pode ver alguns exemplos na própria raiz do repositório. 

O Google tem uma página bem explicativa sobre como [formatar o SSML](https://cloud.google.com/text-to-speech/docs/ssml?hl=pt-br).
