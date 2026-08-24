# 🧪 Testes de Aplicação Web — Reserva e Pagamento

## 📌 Sobre o projeto

Este projeto foi desenvolvido com o objetivo de realizar testes em uma aplicação web de reservas, verificando se os principais recursos funcionam conforme o esperado.

Durante os testes, foram avaliados pontos como layout da aplicação, preenchimento de campos, fluxo de reserva, método de pagamento, cadastro de cartão, botão de reservar e cancelamento de uma reserva.

A ideia foi colocar em prática conceitos de **Quality Assurance (QA)**, identificando comportamentos que estavam de acordo com o esperado e também possíveis problemas na aplicação.

---

## 🎯 Objetivo

Validar o funcionamento dos principais recursos da aplicação e identificar possíveis falhas durante a execução dos testes.

Os testes foram realizados considerando diferentes cenários, incluindo preenchimento correto e incorreto dos campos, validações, limites de caracteres, fluxos de sucesso e situações em que o sistema deveria impedir a continuidade da ação.

---

## 🧪 Técnicas de teste utilizadas

* Teste funcional
* Teste exploratório
* Teste de validação de campos
* Teste de cenários positivos e negativos
* Teste de interface e layout

---

## 📊 Casos de testes executados

Ao todo, foram executados **159 testes** durante o projeto.

| Resultado           | Quantidade |
| ------------------- | ---------: |
| ✅ Aprovados         |        129 |
| ❌ Reprovados        |         30 |
| 🐞 Bugs encontrados |         30 |

Os testes reprovados foram analisados e os problemas encontrados foram registrados para facilitar o acompanhamento e a correção das falhas.

---

## 🔎 Cenários testados

### Layout da aplicação

Foram realizadas validações relacionadas à interface da aplicação, incluindo:

* Organização dos elementos;
* Campos de origem e destino;
* Mapa e seus controles;
* Informações dos veículos;
* Botões e componentes da tela;
* Informações apresentadas durante uma reserva.

### Método de pagamento

Foram testados os principais comportamentos relacionados ao pagamento:

* Abertura da janela de método de pagamento;
* Cadastro de cartão;
* Validação dos campos;
* Limites de caracteres;
* Preenchimento válido e inválido;
* Botão de adicionar;
* Botão de cancelar;
* Adição de mais de um cartão.

### Botão "Reservar"

Foram realizados testes para verificar o comportamento do botão de reserva em diferentes situações, como:

* Todos os campos preenchidos;
* Carteira de motorista não cadastrada;
* Método de pagamento não informado;
* Campos obrigatórios vazios;
* Endereços preenchidos ou removidos.

### Reserva e cancelamento

Também foram realizados testes no fluxo de reserva, verificando:

* Criação de uma reserva;
* Exibição das informações do veículo;
* Valor e tempo de espera;
* Exibição das informações da viagem;
* Funcionamento do botão de cancelamento.

---

## 🐞 Bugs encontrados

Durante a execução dos testes foram identificados **30 bugs**, que foram registrados para acompanhamento.

Os problemas encontrados envolveram principalmente:

* Validação de campos;
* Comportamento de componentes da interface;
* Exibição de informações;
* Fluxo de reserva;
* Método de pagamento;
* Cancelamento de reserva.

Os bugs foram registrados no **Jira**, permitindo acompanhar cada problema individualmente.

---

## 🛠️ Ferramentas utilizadas

* **Planilhas Excel** — criação dos checklists e registro dos resultados;
* **Jira** — registro e acompanhamento dos bugs;
* **Google Chrome** — execução dos testes;
* **Mozilla Firefox** — execução dos testes.

---

## 📁 Estrutura do projeto

A planilha utilizada para organização dos testes foi dividida em quatro partes:

```text
📂 Projeto - Teste de Aplicativo Web
│
├── 1. Checklist do layout
├── 2. Checklist - Método de pagamento
├── 3. Casos de teste - Botão Reservar
└── 4. Casos de teste - Reserva
```

Cada parte possui seus respectivos cenários, resultados esperados, status dos testes e, quando necessário, o link para o bug encontrado.

---

## 💡 Conclusão

A execução dos testes permitiu validar diferentes partes da aplicação e encontrar problemas que poderiam afetar a experiência do usuário.

No total, foram **159 testes executados**, sendo **129 aprovados e 30 reprovados**, com 30** bugs identificados e registrados**.

Esse projeto foi uma oportunidade para praticar a criação de casos de teste, execução de cenários positivos e negativos, identificação de bugs e organização dos resultados de uma forma mais próxima de um projeto real de QA.

---

### 👨‍💻 Autor

**Miqueias Ferreira**

Projeto desenvolvido para prática e demonstração de conhecimentos em **Quality Assurance (QA) e testes de software**.

