# 🧾 Senai_LLP_EnumGen_Pedido

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Status](https://img.shields.io/badge/status-conclu%C3%ADdo-brightgreen)
![Contexto](https://img.shields.io/badge/contexto-acad%C3%AAmico%20SENAI%2FFATESG-blue)

## 📌 Sobre o projeto

Programa de console em Java que simula o cadastro de itens de um pedido, permitindo informar a descrição, a quantidade e a categoria de cada item até que o usuário decida finalizar a entrada. Foi desenvolvido na disciplina de **Linguagem e Lógica de Programação (LLP)** do curso de **Análise e Desenvolvimento de Sistemas do SENAI/FATESG**.

## 🎯 Objetivo

Praticar o uso de **classes próprias como estrutura de dados** (uma classe `Item` para representar cada item do pedido), o armazenamento de múltiplos objetos em uma coleção genérica (`List<Item>`), laços de repetição controlados pelo usuário e validação básica de entrada de dados.

## 🛠️ O que foi desenvolvido

Um único programa, `OrdemPedido.java`, que:

- Define uma classe interna `Item`, com os atributos `categoria`, `descricao` e `quantidade`;
- Em um laço controlado pelo usuário, pede a descrição de um item — uma entrada vazia encerra o cadastro;
- Pede a quantidade do item, validando que o valor digitado é um número inteiro;
- Apresenta uma lista fixa de categorias (`Alimento`, `Eletrônico`, `Outros`) para o usuário escolher por número, validando a opção;
- Ao final, cadastra o item na lista e, quando o usuário encerra a entrada, imprime todos os itens cadastrados.

## ⚙️ Como funciona

O fluxo de execução é interativo, via terminal:

1. O programa pede a descrição do item (`Scanner.nextLine()`); se vazia, o cadastro é encerrado;
2. Pede a quantidade, tratando com `try/catch (NumberFormatException)` o caso de uma entrada não numérica;
3. Mostra o menu de categorias e repete a pergunta até receber uma opção válida (`while (true)` com validação);
4. Cria um novo objeto `Item` com os dados informados e o adiciona a uma `List<Item>`;
5. Repete o processo até a descrição vazia, e então imprime todos os itens cadastrados, um por linha.

Para executar:

```bash
javac OrdemPedido.java
java OrdemPedido
```

## 💻 Tecnologias utilizadas

- **Java (SE)** — linguagem do projeto, sem dependências externas.
- **`java.util.Scanner`** — leitura de toda a entrada do usuário via terminal.
- **`java.util.List` e `java.util.ArrayList`** — armazenamento dos objetos `Item` cadastrados durante a execução.
- **Classe própria (`Item`)** — modelagem simples de um tipo de dado do domínio do problema (um item de pedido), com construtor e atributos públicos.
- **Tratamento de exceções (`try/catch`)** — usado para validar a quantidade digitada e evitar que uma entrada inválida derrube o programa.
- **Laços `while`** — tanto para o cadastro repetido de itens quanto para a validação da categoria escolhida.

## ✅ Principais funcionalidades

- Cadastro de múltiplos itens em uma mesma execução, encerrado por uma entrada vazia.
- Seleção de categoria por menu numerado, com nova tentativa em caso de opção inválida.
- Validação de quantidade não numérica sem interromper o programa.
- Listagem final de todos os itens cadastrados na sessão.

## 📚 O que foi aprendido

- Como agrupar dados relacionados (descrição, quantidade, categoria) em uma classe própria em vez de usar variáveis soltas.
- Diferença entre `Scanner.nextInt()` e `Scanner.nextLine()` e os cuidados necessários ao misturar os dois métodos de leitura.
- Construção de menus simples no console com validação de opção do usuário.
- Uso de coleções genéricas (`List<Item>`) para guardar um número variável de registros.

## 🎓 Contexto acadêmico

Este projeto faz parte do conjunto de **primeiros repositórios que publiquei no GitHub** durante a minha formação em **Análise e Desenvolvimento de Sistemas no SENAI/FATESG**. Ele documenta uma etapa inicial da minha evolução como desenvolvedor, com foco em fixar lógica de programação e modelagem simples de dados em Java — antes de aplicar padrões de projeto, camadas de arquitetura ou frameworks, que vieram em trabalhos posteriores.

## ⚠️ Observações

- O nome do repositório faz referência a "Enum", mas a implementação atual resolve a seleção de categoria com um array de `String` e validação manual, não com um `enum` do Java — uma diferença entre a intenção do exercício e a versão que ficou registrada neste repositório, mantida aqui sem alterações por já fazer parte do histórico do projeto.
- É um programa de console simples, sem persistência de dados (os itens cadastrados existem apenas durante a execução) e sem testes automatizados, características típicas de um exercício introdutório de lógica de programação.

## 👤 Autor

**João Pedro Abdala** — estudante de Análise e Desenvolvimento de Sistemas (SENAI/FATESG)
[github.com/joaoabdala05](https://github.com/joaoabdala05)
