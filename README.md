# 🧪 QA - Testes Funcionais e Análise de Classes de Equivalência

## 📋 Sobre o projeto

Este repositório apresenta a documentação e a execução de testes funcionais realizados em um formulário de cadastro, com foco na validação dos campos e das regras de negócio relacionadas às entradas fornecidas pelo usuário.

O projeto foi desenvolvido utilizando técnicas de **Teste Caixa-Preta**, principalmente:

* **Particionamento por Classes de Equivalência**
* **Análise de Valores-Limite**
* **Validação de entradas válidas e inválidas**
* **Testes de restrições de caracteres**
* **Testes de tamanho mínimo e máximo dos campos**

A documentação foi organizada para demonstrar o processo de planejamento, criação e execução dos casos de teste.

---

# 🎯 Objetivo

O objetivo principal deste projeto é validar se os campos do formulário se comportam de acordo com as regras estabelecidas, garantindo que:

* Entradas válidas sejam aceitas corretamente;
* Entradas inválidas sejam rejeitadas;
* Os limites mínimos e máximos sejam respeitados;
* Caracteres não permitidos sejam identificados;
* Mensagens de erro sejam apresentadas quando necessário;
* O comportamento da aplicação esteja de acordo com o resultado esperado para cada cenário.

---

# 🧠 Técnicas de teste utilizadas

## 1. Particionamento por Classes de Equivalência

A técnica de Particionamento por Classes de Equivalência foi utilizada para dividir os dados de entrada em grupos que devem apresentar comportamentos semelhantes.

Em vez de testar todas as possibilidades existentes, são selecionados valores representativos de cada classe.

Exemplo para um campo que aceita nomes entre **2 e 14 caracteres**:

### Classe válida

| Regra                        | Exemplos                                       |
| ---------------------------- | ---------------------------------------------- |
| Nome entre 2 e 14 caracteres | `Su`, `Gil`, `caio oliveira`, `Pedro Henrique` |

### Classes inválidas

| Regra                          | Exemplos                           |
| ------------------------------ | ---------------------------------- |
| Nome com apenas 1 caractere    | `S`                                |
| Nome com 15 caracteres ou mais | Valores acima do limite permitido  |
| Caracteres especiais           | `mi-queias`                        |
| Símbolos                       | `@Miqueias`                        |
| Números                        | `miqueias12`                       |
| Letras não latinas             | Caracteres fora do conjunto aceito |
| Campo vazio                    | `""`                               |

---

## 2. Análise de Valores-Limite

Além das classes de equivalência, foram considerados valores próximos aos limites definidos pelas regras de negócio.

Para o campo **Nome**, foram testados cenários relacionados a:

* Limite inferior inválido: **1 caractere**
* Limite inferior válido: **2 caracteres**
* Valores válidos intermediários: **3 e 13 caracteres**
* Limite superior válido: **14 caracteres**
* Limite superior inválido: **15 caracteres**
* Valores acima do limite: **16 caracteres**

Essa abordagem permite identificar possíveis falhas relacionadas às fronteiras das regras de validação.

---

# 🔍 Escopo dos testes

A documentação do projeto contempla análises de equivalência para diferentes campos, incluindo:

* Nome
* Sobrenome
* Data de nascimento

Os **casos de teste efetivamente documentados com status de execução na planilha analisada** concentram-se na validação do campo **Nome**, dentro do fluxo:

> **Adicionar carteira de motorista**

---

# 🧪 Casos de teste executados

Foram documentados e executados **14 casos de teste**.

| ID   | Cenário testado                     | Resultado  |
| ---- | ----------------------------------- | ---------- |
| T-1  | Nome com 2 caracteres               | ✅ Aprovado |
| T-2  | Nome contendo apenas letras latinas | ✅ Aprovado |
| T-3  | Nome com letras não latinas         | ✅ Aprovado |
| T-4  | Nome contendo espaço                | ✅ Aprovado |
| T-5  | Nome contendo símbolos              | ✅ Aprovado |
| T-6  | Nome contendo caracteres especiais  | ✅ Aprovado |
| T-7  | Nome contendo números               | ✅ Aprovado |
| T-8  | Nome com apenas 1 caractere         | ✅ Aprovado |
| T-9  | Nome com 15 caracteres              | ✅ Aprovado |
| T-10 | Nome com 16 caracteres              | ✅ Aprovado |
| T-11 | Nome com 3 caracteres               | ✅ Aprovado |
| T-12 | Nome com 13 caracteres              | ✅ Aprovado |
| T-13 | Nome com 14 caracteres              | ✅ Aprovado |
| T-14 | Campo Nome vazio                    | ✅ Aprovado |

---

# 📊 Resumo da execução

## Métricas do projeto

| Métrica                                  | Quantidade |
| ---------------------------------------- | ---------: |
| Casos de teste documentados e executados |     **14** |
| Casos aprovados                          |     **14** |
| Casos reprovados                         |      **0** |
| Taxa de aprovação                        |   **100%** |
| Bugs registrados na documentação         |      **0** |

### 📈 Resultado geral

```text
Total de testes:      14
Testes aprovados:     14
Testes reprovados:    0
Taxa de aprovação:    100%
Bugs registrados:     0
```

> **Observação:** o número de **0 bugs registrados** significa que nenhum defeito foi identificado ou registrado durante a execução dos casos de teste presentes nesta documentação. Esse resultado não garante que a aplicação esteja completamente livre de defeitos, pois o projeto possui um escopo específico de testes.

---

# 🔬 Detalhamento dos principais cenários

## ✅ Entradas válidas

Foram validados cenários em que o sistema deveria aceitar corretamente os dados fornecidos.

Entre os testes realizados estão:

* Nome com 2 caracteres;
* Nome com 3 caracteres;
* Nome com 13 caracteres;
* Nome com 14 caracteres;
* Letras latinas;
* Texto contendo espaço.

O comportamento esperado nesses cenários era a ausência de mensagens de erro no campo.

---

## ❌ Entradas inválidas

Também foram testados cenários em que o sistema deveria impedir ou sinalizar entradas inválidas.

Os cenários incluem:

* Nome com apenas 1 caractere;
* Nome com 15 caracteres;
* Nome com 16 caracteres;
* Campo vazio;
* Utilização de símbolos;
* Utilização de caracteres especiais;
* Utilização de números;
* Utilização de caracteres não latinos.

Nesses casos, o comportamento esperado era a apresentação de uma mensagem de erro no campo.

---

# 📁 Estrutura da documentação

```text
📦 projeto-qa
 ┣ 📄 Projeto documentação de teste.xlsx
 ┃
 ┣ 📂 Classes de equivalência
 ┃ ┣ 📌 Nome
 ┃ ┣ 📌 Sobrenome
 ┃ ┗ 📌 Data de nascimento
 ┃
 ┗ 📂 Casos de teste
   ┣ 📌 T-1
   ┣ 📌 T-2
   ┣ 📌 T-3
   ┣ 📌 ...
   ┗ 📌 T-14
```

A documentação está organizada em duas áreas principais:

### 📘 Classes de equivalência

Contém o planejamento dos testes, incluindo:

* Classes válidas;
* Classes inválidas;
* Limites aceitos;
* Valores fora dos limites;
* Dados de teste;
* Cenários relacionados aos campos analisados.

### 📗 Casos de teste

Contém os cenários executados, apresentando informações como:

* ID do caso de teste;
* Nome do cenário;
* Pré-condições;
* Etapas de execução;
* Resultado esperado;
* Status final.

---

# 🛠️ Ferramentas utilizadas

* **Microsoft Excel** — Documentação e organização dos casos de teste;
* **Testes Manuais** — Execução dos cenários;
* **Técnicas de Teste Caixa-Preta** — Definição das estratégias de validação.

---

# 📚 Conceitos aplicados

Durante o desenvolvimento deste projeto foram aplicados conceitos fundamentais de Quality Assurance, incluindo:

* Testes funcionais;
* Testes manuais;
* Teste Caixa-Preta;
* Classes de Equivalência;
* Análise de Valores-Limite;
* Cenários positivos;
* Cenários negativos;
* Resultado esperado;
* Registro do status de execução.

---

# 🚀 Possíveis melhorias futuras

O projeto pode ser expandido com novas etapas e tipos de teste, como:

* [ ] Criação de casos de teste completos para todos os campos analisados;
* [ ] Execução dos cenários de Sobrenome;
* [ ] Execução dos cenários de Data de Nascimento;
* [ ] Registro detalhado de defeitos encontrados;
* [ ] Inclusão de severidade e prioridade dos bugs;
* [ ] Criação de evidências de teste;
* [ ] Inclusão de screenshots dos resultados;
* [ ] Automação dos principais cenários;
* [ ] Testes de regressão;
* [ ] Testes de integração;
* [ ] Relatórios de execução mais detalhados.

---

# 📌 Conclusão

Este projeto demonstra a aplicação prática de técnicas fundamentais de **Quality Assurance** para a criação e execução de testes funcionais.

Foram realizados **14 casos de teste documentados**, com **100% de aprovação** e **nenhum bug registrado dentro do escopo e da documentação analisados**.

A estratégia adotada permitiu validar diferentes comportamentos do campo **Nome**, incluindo entradas válidas, inválidas e valores próximos aos limites definidos pelas regras de negócio.

O projeto também apresenta uma base estruturada para futuras expansões, permitindo a inclusão de novos cenários, campos, evidências, relatórios de bugs e testes automatizados.

---

## 👨‍💻 Autor

**Miqueias Ferreira**

Projeto desenvolvido para prática e aplicação de conceitos de **Quality Assurance (QA)**, **Testes Funcionais** e **Teste Caixa-Preta**.
