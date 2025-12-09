# TT&C

> Todo o trabalho de TT&C foi desenvolvido nesse repositório

[Link para repositório](https://github.com/lanalvgon/TTeC_trainee_GCD)

Este módulo concentra o desenvolvimento do **subsistema de TT&C (Telemetria, Telecomando e Comunicação)** do CubeSat **ECOVISION**, realizado no contexto do **Projeto Trainee 2025 da Gama Cube Design**.

Os códigos foram desenvolvidos e testados utilizando o **microcontrolador ESP32** em conjunto com os módulos **LoRa RA-01 e RA-02**, permitindo a comunicação entre o **satélite (sat)** e a **estação de solo (ground)**.

## Organização do diretório do projeto

A estrutura do repositório foi organizada de forma separada para representar claramente os dois lados da comunicação:

- `ground.ino`  
  Contém o código-fonte responsável pela **comunicação da Ground Station**.

- `sat.ino`  
  Contém o código-fonte final responsável pela **comunicação do Satélite**.

Essa separação facilita os testes independentes de cada ponta da comunicação e garante uma melhor organização do desenvolvimento.


## Como utilizar o módulo de TT&C

Este módulo é utilizado principalmente por meio da **IDE do Arduino** ou do **Arduino CLI**, visto que os códigos são desenvolvidos no formato `.ino`.

De forma geral, o fluxo de uso é:

1. Abrir o arquivo correspondente:
   - `ground.ino` para a estação de solo  
   - `sat.ino` para o satélite  

2. Conectar o microcontrolador **ESP32** ao computador via USB.

3. Selecionar a porta e a placa corretamente na IDE.

4. Compilar e enviar o código para o dispositivo.

Cada pasta representa um sistema completo e independente para testes de comunicação.


## Estado Atual do Módulo

Atualmente, o módulo de TT&C conta com:

- Comunicação implementada entre **satélite e estação de solo**
- Testes realizados com **ESP32 + LoRa RA-01 / RA-02**
- Estrutura organizada por lado de comunicação (ground / sat)

Este módulo futuramente será integrado com o **OBC** e com os demais sistemas do satélite.


## Autoria

Projeto desenvolvido por:

- **[Lana Alves](https://github.com/lanalvgon)**
- **[Maria Eduarda Gomes](https://github.com/dudandrad)**

No contexto do **Projeto Trainee 2025 – Gama Cube Design**.

---

<div align="center">
  <a href="https://github.com/BrunoBReis/GCD-eletroncia-trainee-2025.2/tree/main/ttec" target="_blank">
    <button style="
      padding: 10px 20px;
      font-size: 16px;
      font-weight: bold;
      border-radius: 8px;
      border: none;
      cursor: pointer;
      background-color: #6f42c1;
      color: white;
    ">
      Acessar Código do TT&C
    </button>
  </a>
</div>
