# gopabx
Um gerador de textos para URAs feito em Go (Golang), que utiliza as APIs de text-to-speech to Google Cloud.

## Importante
Para usar esse app, você precisará configurar sua conta no Google Cloud, projeto, credenciais, etc. Eu não poderia explicar melhor do que faz o Google [aqui](https://cloud.google.com/text-to-speech/docs/quickstart-client-libraries?hl=pt-br).

A propósito, meu código usa como base o código disponível no Guia de início rápido do artigo linkado acima, com algumas diferenças:

1. Eu setei a única voz (feminina, baseada em Wavenet) disponível em português do Brasil.
1. Ao invés de utilizar uma `string` dentro do próprio código, meu código espera receber um arquivo `ssml` como argumento na linha de comando, por exemplo:

`go run main.go -ssml=arquivo.ssml`

Se o nome é `arquivo.ssml`, ao terminar o app terá gerado um mp3 de nome `arquivo.mp3` no diretório raiz da aplicação.
