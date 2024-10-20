# Go Multithreading

> [!IMPORTANT]  
> Para poder executar o projeto contido neste repositório é necessário que se tenha o Go instalado no computador. Para maiores informações siga o site <https://go.dev/>

## Desafio GoLang Pós GoExpert - Multithreading

Este projeto faz parte como desafio da Pós GoExpert, nele são cobertos os conhecimentos em Go Routines, channels, contextos, tratamentos de erros.

O Desafio consiste em entregar um sistema em Go, onde ele deve realizar a busca de CEP em duas APIs distintas e nos trazer o resultado que da API que nos responder mais rápido. As APIs a serem utilizadas serão a seguintes:

```plaintext
A - https://brasilapi.com.br/api/cep/v1/01153000 + cep
B - http://viacep.com.br/ws/ + cep + /json
```

Temos os seguintes requisitos a serem seguidos:

- As duas requisições, devem ser realizadas simultaneamente;
- Acatar a API que entregar a resposta mais rápida e descartar a resposta mais lenta;
- Limitar o tempo de resposta em 1 segundo, Caso contrário, o erro de timeout deve ser exibido.

## Extras Adicionados no Desafio

Por conta de questões como boas práticas, decidi adicionar alguns pontos extras no exercício, como por exemplo:

- Validação do CEP;
    > Valida se a informação tem o tamanho de um CEP (8) e é formada apenas por dígitos.

- Carregamento das URL de variáveis de ambiente;
    > Ao invés das URL's das API's serem inputadas diretamente `hardcoded` coloquei elas sendo passadas por variáveis de ambiente, de forma que no caso de uma mudança, ou troca de API's, desde que obdeça o mesmo contrato não haja necessidade de mexer no código.

### Executando os sistemas

Para executar o sistema, basta executar o comando abaixo, sempre passando como argumento um cep válido.

```shell
❯ go run main.go 21810020
```

Na janela do terminal você deverá ver uma mensagem parecida com o exemplo abaixo:

```shell
❯ go run main.go 21831430
API BrasilAPI :: resposta (86.366792ms) - {Cep:21831430 Logradouro:Rua Júlio Conceição Complemento: Bairro:Senador Camará Localidade:Rio de Janeiro Uf:RJ}
```
