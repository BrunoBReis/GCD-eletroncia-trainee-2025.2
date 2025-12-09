# OBC

> Todo o trabalho de OBC foi desenvolvido nesse repositório

[Link para repositório](https://github.com/Pwdrinho/OBC-2025.2)

Este módulo concentra o desenvolvimento do **OBC (On-Board Computer)**, responsável pelo **processamento central do satélite**, incluindo a **leitura de sensores**, organização dos dados internos e a futura integração com os subsistemas de **TT&C** e **Sensoriamento**.

Atualmente, o desenvolvimento está focado na **estrutura básica do software embarcado** e na **captura dos dados dos sensores de temperatura e saúde da bateria**.


## Organização do diretório do projeto

A estrutura do repositório está organizada de forma simples, seguindo um modelo direto para desenvolvimento embarcado:

- `main.c`  
  Arquivo principal do OBC, responsável pela execução do sistema e pela **leitura dos sensores**.

- `data/`  
  Diretório gerado pelo próprio sistema, responsável por armazenar os arquivos de saída com os dados dos sensores:

  - `ds18b20.json` → dados de **temperatura**
  - `ina219.json` → dados de **tensão, corrente e saúde da bateria**

Além disso, o repositório também contém arquivos auxiliares como:

Essa estrutura representa a **base inicial do desenvolvimento do computador de bordo**, com foco em aquisição de dados essenciais para o funcionamento do satélite.


## Como utilizar o módulo de OBC

Este módulo é utilizado por meio de um **ambiente de desenvolvimento em C/C embarcado** ou ferramentas compatíveis com o microcontrolador utilizado.

De forma geral, o fluxo de uso é:

1. Abrir o projeto do OBC no ambiente de desenvolvimento.
2. Conectar o microcontrolador responsável pelo OBC via USB.
3. Compilar o arquivo `main.c`.
4. Enviar o código para o dispositivo.
5. Acompanhar a geração dos arquivos `.json` para validação dos sensores.

---

## Estado Atual do Módulo

Atualmente, o módulo de OBC conta com:

- Estrutura inicial do sistema embarcado
- Leitura implementada de sensores:
  - Temperatura (DS18B20)
  - Saúde da bateria (INA219)
- Geração automática de arquivos `.json` com os dados
- Módulo em fase de desenvolvimento e expansão
- Base preparada para integração com TT&C e Sensoriamento

Este módulo será o **núcleo lógico do satélite**, sendo responsável pelo gerenciamento das missões e da operação embarcada.


## Autoria

Projeto desenvolvido por:

- **[Pedro Lucas](https://github.com/Pwdrinho)**
- **[Pedro Henrique](https://github.com/phenric26)**

---

<div align="center">
  <a href="https://github.com/BrunoBReis/GCD-eletroncia-trainee-2025.2/blob/main/obc/main.c" target="_blank">
    <button style="
      padding: 10px 20px;
      font-size: 16px;
      font-weight: bold;
      border-radius: 8px;
      border: none;
      cursor: pointer;
      background-color: #2ea44f;
      color: white;
    ">
      Acessar Código do OBC
    </button>
  </a>
</div>
