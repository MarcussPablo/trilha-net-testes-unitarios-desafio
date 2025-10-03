# DIO - Trilha .NET - Testes Unitários com C#
www.dio.me

## Desafio de Projeto
Este projeto faz parte da trilha .NET da DIO e tem como objetivo aplicar os conhecimentos de **Testes Unitários com C# e xUnit**.

## Contexto
Durante o desenvolvimento de sistemas, é comum surgirem problemas como bugs, funcionalidades que deixam de funcionar de forma inesperada e falhas em validações. Para aumentar a confiabilidade do código e garantir qualidade, foram implementados testes unitários cobrindo os cenários principais (positivos e negativos).  

O projeto contém duas classes principais com lógicas de validação (**ValidacoesLista** e **ValidacoesString**) e um projeto de testes que garante o correto funcionamento desses métodos.

## Estrutura da Solução
A solução é composta por dois projetos:

- **TestesUnitarios.Desafio.Console**  
  Projeto console que contém as classes de validação.

- **TestesUnitarios.Desafio.Tests**  
  Projeto de testes, utilizando **xUnit**, que valida os métodos do projeto console.

Estrutura de diretórios:

trilha-net-testes-unitarios-desafio
│
├── TestesUnitarios.Desafio.Console
│ └── Services
│ ├── ValidacoesLista.cs
│ └── ValidacoesString.cs
│
├── TestesUnitarios.Desafio.Tests
│ ├── ValidacoesListaTests.cs
│ └── ValidacoesStringTests.cs
│
└── Imagens
└── projeto.png


## Classes do Projeto Console

### Classe **ValidacoesLista**
Responsável por realizar diversas validações envolvendo listas.

| Método                       | Objetivo                                                                                           |
|------------------------------|---------------------------------------------------------------------------------------------------|
| RemoverNumerosNegativos      | Recebe uma lista de inteiros e retorna uma nova lista apenas com os números positivos              |
| ListaContemDeterminadoNumero | Verifica se um número específico está presente na lista                                           |
| MultiplicarNumerosLista      | Retorna uma nova lista com todos os valores multiplicados por um número informado                 |
| RetornarMaiorNumeroLista     | Retorna o maior número dentro da lista                                                            |
| RetornarMenorNumeroLista     | Retorna o menor número dentro da lista                                                            |

### Classe **ValidacoesString**
Responsável por realizar diversas validações envolvendo strings.

| Método                       | Objetivo                                                                                           |
|------------------------------|---------------------------------------------------------------------------------------------------|
| RetornarQuantidadeCaracteres | Retorna a quantidade de caracteres de um texto                                                    |
| ContemCaractere              | Verifica se um determinado trecho existe dentro de um texto                                       |
| TextoTerminaCom              | Verifica se um texto termina com um determinado trecho                                            |

## Classes de Teste (xUnit)

### Classe **ValidacoesListaTests**
| Método de teste                               | Cenário Validado                                                                                      |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------|
| DeveRemoverNumerosNegativosDeUmaLista         | Lista com positivos e negativos deve retornar apenas positivos                                        |
| DeveConterONumero9NaLista                     | Deve retornar verdadeiro quando a lista contém o número 9                                             |
| NaoDeveConterONumero10NaLista                 | Deve retornar falso quando a lista não contém o número 10                                             |
| DeveMultiplicarOsElementosDaListaPor2         | Deve retornar nova lista com todos os elementos multiplicados por 2                                   |
| DeveRetornar9ComoMaiorNumeroDaLista           | Deve retornar 9 como o maior número da lista                                                          |
| DeveRetornarOitoNegativoComoMenorNumeroDaLista| Deve retornar -8 como o menor número da lista                                                         |

### Classe **ValidacoesStringTests**
| Método de teste                                  | Cenário Validado                                                                                      |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| DeveRetornar6QuantidadeCaracteresDaPalavraMatrix | Deve retornar 6 ao contar os caracteres da palavra "Matrix"                                           |
| DeveContemAPalavraQualquerNoTexto                | Deve retornar verdadeiro quando o texto contém a palavra "qualquer"                                   |
| NaoDeveConterAPalavraTesteNoTexto                | Deve retornar falso quando o texto não contém a palavra "teste"                                       |
| TextoDeveTerminarComAPalavraProcurado            | Deve retornar verdadeiro quando o texto termina com a palavra "procurado"                             |

## Execução dos Testes

Para rodar os testes, basta executar no diretório da solução:

```bash
dotnet test

Resultado

Aprovado!  – Com falha:     0, Aprovado:    10, Ignorado:     0, Total:    10
Estrutura Visual do Projeto
![Texto alternativo](./Imagens/projeto.png)


---

Marcus, esse `README.md` já tá no **formato de entrega**, mostrando que todos os testes foram implementados e passaram ✅.  

Quer que eu deixe ainda mais "acadêmico" (com seção de **Aprendizados** no final), ou melhor manter direto e objetivo só mostrando que o desafio foi concluído?
