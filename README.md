# DESAFIO-QA-BEEDOO-2026

## Sobre o desafio

Este repositório contém a análise, modelagem de testes e execução de testes realizados para o desafio técnico de **Analista de Qualidade de Software Júnior**.

O objetivo do desafio foi explorar uma aplicação web de cadastro e listagem de cursos, identificar possíveis problemas e documentar cenários de teste, evidências e bugs encontrados durante a análise.

Aplicação testada:

https://creative-sherbet-a51eac.netlify.app/

---

## Análise inicial da aplicação

A aplicação analisada consiste em um sistema web simples para **cadastro e gerenciamento de cursos**. Durante a exploração inicial da aplicação, foi possível identificar algumas funcionalidades principais relacionadas ao registro e visualização de cursos.

Com base nessa análise, foram identificados os seguintes fluxos principais do sistema:

### 1. Cadastro de curso
Fluxo em que o usuário preenche um formulário com as informações do curso e realiza o cadastro no sistema.

### 2. Listagem de cursos
Fluxo responsável por exibir os cursos cadastrados, apresentados em formato de cards contendo as principais informações de cada curso.

### 3. Exclusão de curso
Fluxo que permite ao usuário remover cursos previamente cadastrados no sistema.

### 4. Visualização das informações do curso
Após o cadastro, os cursos passam a ser exibidos na listagem, permitindo a visualização das informações básicas cadastradas para cada curso.

---

## Pontos críticos do sistema para teste

Durante a análise inicial da aplicação, foi possível identificar alguns pontos considerados críticos para a qualidade e funcionamento do sistema.

### Cadastro de cursos

O fluxo de cadastro de cursos foi considerado o ponto mais crítico da aplicação, pois é responsável pela entrada de dados no sistema.  
Grande parte das funcionalidades da aplicação depende diretamente das informações cadastradas nesse fluxo.

Caso ocorram falhas nesse processo, funcionalidades como a listagem e visualização de cursos podem ser impactadas.

Por esse motivo, foram realizados diversos testes relacionados a:

- validação de campos obrigatórios
- formatos de entrada
- limite de caracteres
- validação de datas
- verificação de duplicidade de cursos

### Integridade dos dados

Também foi considerado importante verificar se os dados cadastrados são armazenados e exibidos corretamente na listagem de cursos.

### Regras de negócio

Foram avaliadas regras de comportamento esperadas do sistema, como:

- validação de datas de início e término
- comportamento para cursos presenciais e online
- consistência das informações exibidas

### Funcionalidade de exclusão

A exclusão de cursos também foi considerada um ponto relevante, pois envolve remoção de dados do sistema e pode impactar diretamente a integridade das informações exibidas.

### Interface e experiência do usuário

Além das funcionalidades principais, também foram observados aspectos relacionados à experiência do usuário, como:

- organização da listagem de cursos
- responsividade da interface
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

## Evidências de execução

As evidências da execução dos testes foram adicionadas diretamente na planilha de testes, na aba **Bugs**, na coluna **Evidências**, contendo registros associados a cada defeito identificado.

As evidências incluem **prints de tela (Imgur)** e **gravações de vídeo realizadas com Jam**, utilizadas para demonstrar o comportamento observado durante a execução dos testes.

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