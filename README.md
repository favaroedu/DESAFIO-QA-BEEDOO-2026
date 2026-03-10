# DESAFIO-QA-BEEDOO-2026

## Sobre o desafio

Este repositório contém a análise, modelagem de testes e execução de testes realizados para o desafio técnico de **Analista de Qualidade de Software Júnior**.

O objetivo do desafio foi explorar uma aplicação web de cadastro e listagem de cursos, identificar possíveis problemas e documentar cenários de teste, evidências e bugs encontrados durante a análise.

Aplicação testada:

https://creative-sherbet-a51eac.netlify.app/

---

# Análise inicial da aplicação

A aplicação consiste em um sistema simples para **cadastro e listagem de cursos**.

Durante a exploração inicial, foi possível identificar que o sistema permite ao usuário:

- Cadastrar novos cursos
- Listar cursos cadastrados
- Excluir cursos
- Visualizar informações básicas de cada curso

A interface é simples e possui foco principal no gerenciamento de cursos.

---

# Objetivo da aplicação

Com base na análise da interface e funcionalidades disponíveis, o objetivo da aplicação parece ser permitir que usuários possam **registrar e visualizar cursos**, contendo informações como:

- Nome do curso
- Descrição
- Instrutor
- Data de início e término
- Tipo do curso (online ou presencial)
- Informações adicionais como endereço ou link de inscrição

A aplicação parece simular um sistema de **gerenciamento de cursos ou treinamentos**.

---

# Principais fluxos disponíveis

Durante a exploração da aplicação, foram identificados os seguintes fluxos principais:

### 1. Cadastro de curso

Fluxo onde o usuário preenche um formulário contendo informações do curso e realiza o cadastro no sistema.

### 2. Listagem de cursos

Fluxo responsável por exibir os cursos cadastrados no sistema em formato de cards.

### 3. Exclusão de curso

Fluxo onde o usuário pode remover cursos previamente cadastrados.

### 4. Visualização das informações do curso

Após o cadastro, os cursos são exibidos na listagem com suas informações básicas.

---

# Pontos críticos do sistema para teste

Durante a análise inicial, alguns pontos foram considerados mais críticos para testes:

### Validação de campos

O sistema depende de dados inseridos pelo usuário, portanto é importante validar:

- campos obrigatórios
- formatos de entrada
- limite de caracteres
- validação de datas

### Integridade dos dados

Garantir que os dados cadastrados sejam exibidos corretamente na listagem de cursos.

### Regras de negócio

Verificar comportamentos esperados como:

- impedir cadastro duplicado
- validar datas de início e término
- exibir corretamente dados específicos de cursos online ou presenciais

### Funcionalidade de exclusão

A exclusão de cursos é uma funcionalidade crítica, pois envolve remoção de dados do sistema.

### Interface e experiência do usuário

Também foram observados aspectos relacionados a:

- responsividade
- organização da listagem de cursos
- clareza das informações exibidas

---

# Decisões tomadas para criação dos testes

Para garantir uma boa cobertura de testes, foram considerados diferentes tipos de cenários:

### Cenários positivos

Testes para validar se o sistema funciona corretamente quando os dados são inseridos conforme esperado.

### Cenários negativos

Testes com entradas inválidas ou incompletas para verificar como o sistema reage a erros.

### Testes de validação

Foram criados testes focados em validação de campos e regras de negócio.

### Testes exploratórios

Durante a análise da aplicação, também foram realizados testes exploratórios para identificar possíveis comportamentos inesperados.

### Testes básicos de segurança

Foi realizado um teste simples de **injeção de script (XSS)** para verificar se a aplicação trata corretamente entradas potencialmente maliciosas.

---

# Explicação do raciocínio durante a análise

A análise da aplicação foi conduzida inicialmente de forma exploratória, com o objetivo de compreender os fluxos disponíveis e identificar possíveis pontos de falha.

A partir dessa exploração inicial, foram definidos cenários de teste considerando:

- fluxo principal da aplicação
- possíveis falhas de validação
- comportamentos inesperados
- qualidade da experiência do usuário

Durante a execução dos testes, foram identificados comportamentos que não atendem às expectativas de funcionamento do sistema, os quais foram registrados como **bugs**.

---

# Casos de teste

Os cenários e casos de teste foram documentados em uma planilha do Google Sheets.

A planilha contém duas abas:

- **Cenário de teste**: contém todos os cenários criados e o resultado da execução dos testes.
- **Bugs**: contém o registro dos defeitos encontrados durante a execução dos testes, incluindo título do bug, passos para reprodução, resultado atual, resultado esperado, severidade e evidências.

Link da planilha:

[Clique aqui para acessar a planilha](https://docs.google.com/spreadsheets/d/1VDpkA9Wr8K8uRuCk9kAPmDsEW2vPWa6e4_yavoy2sHk/edit?usp=sharing)

---

# Evidências de execução

As evidências da execução dos testes foram adicionadas diretamente na planilha de testes, na aba **Bugs**, na coluna **Evidências**, contendo prints/videos de links relacionados a cada defeito identificado.

---

# Bugs encontrados

Durante a execução dos testes foram identificados alguns problemas relacionados a:

- validação de campos
- regras de negócio
- inconsistências na interface
- falhas em funcionalidades do sistema

Os bugs foram documentados na planilha de testes com seus respectivos:

- passos para reprodução
- resultado atual
- resultado esperado
- severidade

---

# Conclusão

A aplicação apresenta uma estrutura simples e funcional para cadastro e listagem de cursos, porém foram identificadas algumas oportunidades de melhoria relacionadas principalmente a validação de dados, experiência do usuário e funcionamento de determinadas funcionalidades.

Os testes realizados permitiram identificar possíveis falhas e sugerir melhorias que podem contribuir para aumentar a qualidade e confiabilidade do sistema.