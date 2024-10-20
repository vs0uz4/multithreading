# Go Multi-threading

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

### Executando os sistemas

WIP...
