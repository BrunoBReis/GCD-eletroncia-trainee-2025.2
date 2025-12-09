# Documentação do Projeto Satélite Gama

<p align="center">
  <img src="assets/logo_gama.png" width="180">
</p>

## Visão Geral

Este repositório tem como principal objetivo **centralizar todo o desenvolvimento de software do projeto**, reunindo em um único ambiente organizado os códigos responsáveis pelos diferentes subsistemas do satélite.

A proposta é permitir que qualquer integrante do projeto consiga:

- Centralizar todos os códigos utilizados no trainee;

- Identificar onde cada sistema está sendo desenvolvido;


## Organização Geral do Repositório

A estrutura do repositório foi pensada para ser **modular**, onde cada diretório principal representa um subsistema do satélite ou uma parte essencial da infraestrutura de desenvolvimento e documentação.

De forma geral, temos:

### `docs/`
Diretório responsável por toda a **documentação do projeto**, construída com MkDocs.  
Aqui ficam as páginas que descrevem cada subsistema, além da estrutura geral, imagens, diagramas e materiais de apoio.

### `sensoriamento/`
Diretório dedicado ao **subsistema de Sensoriamento**.  
Aqui estão concentrados os códigos, scripts e imagens relacionados ao processamento e análise das imagens.


###  `ttec/`
Será o diretório destinado ao subsistema de **TT\&C (Telemetria, Telecomando e Comunicação)**.  
Aqui ficarão concentrados os códigos relacionados à comunicação do satélite com a estação de solo.


### `obc/`
Será o diretório responsável pelo **OBC (On-Board Computer)**, onde ficarão os códigos do computador de bordo, controle das tarefas, gerenciamento de estados e integração entre os subsistemas.

## Arquivos de Infraestrutura

Além dos módulos, o repositório possui alguns arquivos fundamentais para o funcionamento do ambiente:

- `CMakeLists.txt` → Sistema de build dos códigos em C/C++  
- `Makefile` → Automatização de tarefas
- `mkdocs.yml` → Configuração da documentação em MkDocs
- `requirements.txt` → Dependências do ambiente Python
- `README.md` → Apresentação geral do repositório no GitHub
